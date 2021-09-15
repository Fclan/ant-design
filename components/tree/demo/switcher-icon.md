

customize collapse/expand icon of tree node

```jsx
import { Tree } from 'antd';
import { DownOutlined } from '@ant-design/icons';

class Demo extends React.Component {
  onSelect = (selectedKeys, info) => {
    console.log('selected', selectedKeys, info);
  };

  render() {
    return (
      <Tree
        showLine
        switcherIcon={<DownOutlined />}
        defaultExpandedKeys={['0-0-0']}
        onSelect={this.onSelect}
        treeData={[
          {
            name: 'parent 1',
            value: '0-0',
            children: [
              {
                name: 'parent 1-0',
                value: '0-0-0',
                children: [
                  {
                    name: 'leaf',
                    value: '0-0-0-0',
                  },
                  {
                    name: 'leaf',
                    value: '0-0-0-1',
                  },
                  {
                    name: 'leaf',
                    value: '0-0-0-2',
                  },
                ],
              },
              {
                name: 'parent 1-1',
                value: '0-0-1',
                children: [
                  {
                    name: 'leaf',
                    value: '0-0-1-0',
                  },
                ],
              },
              {
                name: 'parent 1-2',
                value: '0-0-2',
                children: [
                  {
                    name: 'leaf',
                    value: '0-0-2-0',
                  },
                  {
                    name: 'leaf',
                    value: '0-0-2-1',
                  },
                ],
              },
            ],
          },
        ]}
      />
    );
  }
}

ReactDOM.render(<Demo />, mountNode);
```
