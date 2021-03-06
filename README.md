# gantt-for-react-hourly

> [Frappe Gantt](https://github.com/frappe/gantt) components for React wrapper.

[![Build Status](https://travis-ci.org/hustcc/gantt-for-react.svg?branch=master)](https://travis-ci.org/hustcc/gantt-for-react) [![npm](https://img.shields.io/npm/v/gantt-for-react.svg?style=flat-square)](https://www.npmjs.com/package/gantt-for-react) [![npm](https://img.shields.io/npm/dt/gantt-for-react.svg?style=flat-square)](https://www.npmjs.com/package/gantt-for-react) [![npm](https://img.shields.io/npm/l/gantt-for-react.svg?style=flat-square)](https://www.npmjs.com/package/gantt-for-react)


# 1. install

```sh
npm install gantt-for-react
```


# 2. usage

Online demo see [http://git.hust.cc/gantt-for-react/](http://git.hust.cc/gantt-for-react/).

```js
import React from 'react';
import ReactGantt from 'gantt-for-react';

<ReactGantt 
	tasks={this.getTasks()} 
	viewMode={this.state.viewMode}
	scrollOffsets={this.state.scrollOffsets}

    onClick={this._func} 
	onDateChange={this._func}
	onProgressChange={this._func}
	onViewChange={this._func} 
	customPopupHtml={this._html_func} />
```

Or you can see the code [here](https://github.com/hustcc/gantt-for-react/blob/master/demo/GanttComponent.jsx#L51).

# 3. component props

 - **`tasks`** (required, array)

The tasks array need to be show with gantt graph. task is an object with format: **{ id, name, start, end, progress, dependencies, custom_class }**.

 - **`viewMode`** (required, string)

The view mode of gantt. Can be **Minute, Hour, Quarter Day, Half Day, Day, Week, Month**. 

 - **`scrollOffsets`** (optional, object)

The default scroll offset for different view modes with object format: **{ viewMode : integer }**. ViewMode can be **Minute, Hour, Quarter Day, Half Day, Day, Week, Month**. 

 - **`customPopupHtml`** (optional, func)

The popo html function, can be a function that returns html or a simple html string.

And **4 event function props**: `onClick`, `onDateChange`, `onProgressChange`, `onViewChange`. Document can see [here](https://frappe.github.io/gantt/).


# 4. screenshot

![screenshot](demo/screenshot.png)


# 5. LICENSE

MIT @[hustcc](https://github.com/hustcc)
