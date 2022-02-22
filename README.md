# Stateflow

In kotlin stateflow make it easy to hold position or any other data that we want to hold it. In fragment also it can hold data on rotation. I this example shows spinner slected position in fragment when screen is rotated.

In ViewModel:

 ```
  private val _selectedPosition = MutableStateFlow(0)
  val selectedPosition = _selectedPosition.asStateFlow()

   fun setPosition(position: Int) {
    _selectedPosition.value = position
   }
```

in Fragment
```
  val selectedPosition= viewModel.selectedPosition.value
  spinner.setSelection(selectedPosition) 
	
```

Using this link https://stackoverflow.com/a/71229456/4948924
