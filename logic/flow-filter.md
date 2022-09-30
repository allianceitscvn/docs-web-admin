# Flow filter

Page

Filter

FilterControl

Clear

* oneFilterControl.clear()
  * this.currentValue = null, this.currentFilter = null
* oneFilterControl.updateCurrentValue(null)
  * this.currentValue = null
  * this.updateCurrentFilter(this.getFilterOutFromValue(this.currentValue))
    * filterOut = \_fnGetFilterOutFromValue by type
    * this.currentFilter = filterOut
    * onePage.onChangeFilter()
