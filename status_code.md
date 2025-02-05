# Status Code

## Non-Telemetry RPC Status Code Mapping Table

> **Note**: The status code with asterisk(*) means it is first classification, '🔄' means the code is reserved.

|             Status Code             | QueryRoute | Heartbeat | SendMessage | QueryAssignment | ReceiveMessage | AckMessage | ForwardMessageToDeadLetterQueue | EndTransaction | NotifyClientTermination | ChangeInvisibleDuration |
| :---------------------------------: | :--------: | :-------: | :---------: | :-------------: | :------------: | :--------: | :-----------------------------: | :------------: | :---------------------: | :---------------------: |
|                 OK*                 |     ✅      |     ✅     |      ✅      |        ✅        |       ✅        |     ✅      |                ✅                |       ✅        |            ✅            |            ✅            |
|          MULTIPLE_RESULTS*          |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ✅      |                ❌                |       ❌        |            ❌            |            ❌            |
|            BAD_REQUEST*             |     ❌      |     ❌     |      ❌      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|        ILLEGAL_ACCESS_POINT         |     ✅      |     ❌     |      ❌      |        ✅        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|            ILLEGAL_TOPIC            |     ✅      |     ✅     |      ✅      |        ✅        |       ✅        |     ✅      |                ✅                |       ✅        |            ❌            |            ✅            |
|       ILLEGAL_CONSUMER_GROUP        |     ❌      |     ✅     |      ❌      |        ❌        |       ✅        |     ✅      |                ✅                |       ✅        |            ✅            |            ✅            |
|         ILLEGAL_MESSAGE_TAG         |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|         ILLEGAL_MESSAGE_KEY         |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|        ILLEGAL_MESSAGE_GROUP        |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|    ILLEGAL_MESSAGE_PROPERTY_KEY     |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|       INVALID_TRANSACTION_ID        |     ❌      |     ❌     |      ❌      |        ❌        |       ❌        |     ❌      |                ❌                |       ✅        |            ❌            |            ❌            |
|         ILLEGAL_MESSAGE_ID          |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|      ILLEGAL_FILTER_EXPRESSION      |     ❌      |     ❌     |      ❌      |        ❌        |       ✅        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|       INVALID_RECEIPT_HANDLE        |     ❌      |     ❌     |      ❌      |        ❌        |       ❌        |     ✅      |                ✅                |       ❌        |            ❌            |            ✅            |
| MESSAGE_PROPERTY_CONFLICT_WITH_TYPE |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|      UNRECOGNIZED_CLIENT_TYPE       |     ❌      |     ✅     |      ❌      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ✅            |            ❌            |
|          MESSAGE_CORRUPTED          |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|         CLIENT_ID_REQUIRED          |     ✅      |     ✅     |      ✅      |        ✅        |       ✅        |     ✅      |                ✅                |       ✅        |            ✅            |            ✅            |
|            UNAUTHORIZED*            |     ❌      |     ✅     |      ✅      |        ❌        |       ✅        |     ✅      |                ✅                |       ✅        |            ✅            |            ✅            |
|          PAYMENT_REQUIRED*          |     🔄      |     🔄     |      🔄      |        🔄        |       🔄        |     🔄      |                🔄                |       🔄        |            🔄            |            🔄            |
|             FORBIDDEN*              |     ❌      |     ❌     |      ✅      |        ✅        |       ✅        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|             NOT_FOUND*              |     🔄      |     🔄     |      🔄      |        🔄        |       🔄        |     🔄      |                🔄                |       🔄        |            🔄            |            🔄            |
|          MESSAGE_NOT_FOUND          |     ❌      |     ❌     |      ❌      |        ❌        |       ✅        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|           TOPIC_NOT_FOUND           |     ✅      |     ❌     |      ✅      |        ✅        |       ✅        |     ✅      |                ✅                |       ❌        |            ❌            |            ✅            |
|      CONSUMER_GROUP_NOT_FOUND       |     ❌      |     ❌     |      ❌      |        ❌        |       ✅        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|         PAYLOAD_TOO_LARGE*          |     🔄      |     🔄     |      🔄      |        🔄        |       🔄        |     🔄      |                🔄                |       🔄        |            🔄            |            🔄            |
|       MESSAGE_BODY_TOO_LARGE        |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|        PRECONDITION_FAILED*         |     🔄      |     🔄     |      🔄      |        🔄        |       🔄        |     🔄      |                🔄                |       🔄        |            🔄            |            🔄            |
|         TOO_MANY_REQUESTS*          |     ✅      |     ✅     |      ✅      |        ✅        |       ✅        |     ✅      |                ✅                |       ✅        |            ✅            |            ✅            |
|  REQUEST_HEADER_FIELDS_TOO_LARGE*   |     🔄      |     🔄     |      🔄      |        🔄        |       🔄        |     🔄      |                🔄                |       🔄        |            🔄            |            🔄            |
|    MESSAGE_PROPERTIES_TOO_LARGE     |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|           INTERNAL_ERROR*           |     🔄      |     🔄     |      🔄      |        🔄        |       🔄        |     🔄      |                🔄                |       🔄        |            🔄            |            🔄            |
|        INTERNAL_SERVER_ERROR        |     ✅      |     ✅     |      ✅      |        ✅        |       ✅        |     ✅      |                ✅                |       ✅        |            ✅            |            ✅            |
|          HA_NOT_AVAILABLE           |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|          NOT_IMPLEMENTED*           |     ❌      |     ❌     |      ❌      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|           PROXY_TIMEOUT*            |     ✅      |     ❌     |      ✅      |        ✅        |       ✅        |     ✅      |                ✅                |       ✅        |            ❌            |            ✅            |
|     MASTER_PERSISTENCE_TIMEOUT      |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|      SLAVE_PERSISTENCE_TIMEOUT      |     ❌      |     ❌     |      ✅      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|            UNSUPPORTED*             |     🔄      |     🔄     |      🔄      |        🔄        |       🔄        |     🔄      |                🔄                |       🔄        |            🔄            |            🔄            |
|         VERSION_UNSUPPORTED         |     🔄      |     🔄     |      🔄      |        🔄        |       🔄        |     🔄      |                🔄                |       🔄        |            🔄            |            🔄            |
|   VERIFY_FIFO_MESSAGE_UNSUPPORTED   |     ❌      |     ❌     |      ❌      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |
|     FAILED_TO_CONSUME_MESSAGE*      |     ❌      |     ❌     |      ❌      |        ❌        |       ❌        |     ❌      |                ❌                |       ❌        |            ❌            |            ❌            |

## Server-Client Telemetry RPC Status Code Mapping Table

|                                 | ThreadStackTrace | VerifyMessageResult |
| :-----------------------------: | :--------------: | :-----------------: |
|               OK                |        ✅         |          ✅          |
|         NOT_IMPLEMENTED         |        ✅         |          ❌          |
|    FAILED_TO_CONSUME_MESSAGE    |        ❌         |          ✅          |
| VERIFY_FIFO_MESSAGE_UNSUPPORTED |        ❌         |          ✅          |
|        MESSAGE_CORRUPTED        |        ❌         |          ✅          |
