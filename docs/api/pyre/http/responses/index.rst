:mod:`pyre.http.responses`
==========================

.. py:module:: pyre.http.responses


Module Contents
---------------

.. py:exception:: Continue

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Continue

   .. attribute:: code
      :annotation: = 100

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Request received, please continue

      


.. py:exception:: SwitchingProtocols

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Switching Protocols

   .. attribute:: code
      :annotation: = 101

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Switching to new protocol; obey Upgrade header

      


.. py:exception:: Created

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Created

   .. attribute:: code
      :annotation: = 201

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Document created, URL follows

      


.. py:exception:: Accepted

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Accepted

   .. attribute:: code
      :annotation: = 202

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Request accepted, processing continues off-line

      


.. py:exception:: NonAuthoritativeInformation

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Non-Authoritative Information

   .. attribute:: code
      :annotation: = 203

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Request fulfilled from cache

      


.. py:exception:: NoContent

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   No Content

   .. attribute:: code
      :annotation: = 204

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Request fulfilled, nothing follows

      


.. py:exception:: ResetContent

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Reset Content

   .. attribute:: code
      :annotation: = 205

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Clear input form for further input.

      


.. py:exception:: PartialContent

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Partial Content

   .. attribute:: code
      :annotation: = 206

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Partial content follows.

      


.. py:exception:: MultipleChoices

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Multiple Choices

   .. attribute:: code
      :annotation: = 300

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Object has several resources -- see URI list

      


.. py:exception:: MovedPermanently

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Moved Permanently

   .. attribute:: code
      :annotation: = 301

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Object moved permanently -- see URI list

      


.. py:exception:: Found

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Found

   .. attribute:: code
      :annotation: = 302

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Object moved temporarily -- see URI list

      


.. py:exception:: SeeOther

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   See Other

   .. attribute:: code
      :annotation: = 303

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Object moved -- see Method and URL list

      


.. py:exception:: NotModified

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Not Modified

   .. attribute:: code
      :annotation: = 304

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Document has not changed since given time

      


.. py:exception:: UseProxy

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Use Proxy

   .. attribute:: code
      :annotation: = 305

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = You must use proxy specified in Location to access this resource.

      


.. py:exception:: TemporaryRedirect

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Temporary Redirect

   .. attribute:: code
      :annotation: = 307

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Object moved temporarily -- see URI list

      


.. py:exception:: BadRequestSyntax

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Bad Request

   .. attribute:: code
      :annotation: = 400

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Bad request syntax or unsupported method

      


.. py:exception:: Unauthorized

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Unauthorized

   .. attribute:: code
      :annotation: = 401

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = No permission -- see authorization schemes

      


.. py:exception:: PaymentRequired

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Payment Required

   .. attribute:: code
      :annotation: = 402

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = No payment -- see charging schemes

      


.. py:exception:: Forbidden

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Forbidden

   .. attribute:: code
      :annotation: = 403

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Request forbidden -- authorization will not help

      


.. py:exception:: NotFound

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Not Found

   .. attribute:: code
      :annotation: = 404

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Nothing matches the given URI

      


.. py:exception:: MethodNotAllowed

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Method Not Allowed

   .. attribute:: code
      :annotation: = 405

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Specified method is invalid for this resource.

      


.. py:exception:: NotAcceptable

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Not Acceptable

   .. attribute:: code
      :annotation: = 406

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = URI not available in preferred format.

      


.. py:exception:: ProxyAuthenticationRequired

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Proxy Authentication Required

   .. attribute:: code
      :annotation: = 407

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = You must authenticate with this proxy before proceeding.

      


.. py:exception:: RequestTimeout

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Request Timeout

   .. attribute:: code
      :annotation: = 408

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Request timed out; try again later.

      


.. py:exception:: Conflict

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Conflict

   .. attribute:: code
      :annotation: = 409

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Request conflict.

      


.. py:exception:: Gone

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Gone

   .. attribute:: code
      :annotation: = 410

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = URI no longer exists and has been permanently removed.

      


.. py:exception:: LengthRequired

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Length Required

   .. attribute:: code
      :annotation: = 411

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Client must specify Content-Length.

      


.. py:exception:: PreconditionFailed

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Precondition Failed

   .. attribute:: code
      :annotation: = 412

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Precondition in headers is false.

      


.. py:exception:: RequestEntityTooLarge

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Request Entity Too Large

   .. attribute:: code
      :annotation: = 413

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Entity is too large.

      


.. py:exception:: RequestURITooLong

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Request-URI Too Long

   .. attribute:: code
      :annotation: = 414

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = URI is too long.

      


.. py:exception:: UnsupportedMediaType

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Unsupported Media Type

   .. attribute:: code
      :annotation: = 415

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Entity body in unsupported format.

      


.. py:exception:: RequestedRangeNotSatisfiable

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Requested Range Not Satisfiable

   .. attribute:: code
      :annotation: = 416

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Cannot satisfy request range.

      


.. py:exception:: ExpectationFailed

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Expectation Failed

   .. attribute:: code
      :annotation: = 417

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Expect condition could not be satisfied.

      


.. py:exception:: PreconditionRequired

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Precondition Required

   .. attribute:: code
      :annotation: = 428

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = The origin server requires the request to be conditional.

      


.. py:exception:: TooManyRequests

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Too Many Requests

   .. attribute:: code
      :annotation: = 429

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = The user has sent too many requests in a given amount of time (rate limiting).

      


.. py:exception:: RequestHeaderFieldsTooLarge

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Request Header Fields Too Large

   .. attribute:: code
      :annotation: = 431

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = The server is unwilling to process the request because its header fields are too large.

      


.. py:exception:: InternalServerError

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Internal Server Error

   .. attribute:: code
      :annotation: = 500

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Server got itself in trouble

      


.. py:exception:: NotImplemented

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Not Implemented

   .. attribute:: code
      :annotation: = 501

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Server does not support this operation

      


.. py:exception:: BadGateway

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Bad Gateway

   .. attribute:: code
      :annotation: = 502

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Invalid responses from another server/proxy.

      


.. py:exception:: ServiceUnavailable

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Service Unavailable

   .. attribute:: code
      :annotation: = 503

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = The server cannot process the request due to a high load

      


.. py:exception:: GatewayTimeout

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Gateway Timeout

   .. attribute:: code
      :annotation: = 504

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = The gateway server did not receive a timely response

      


.. py:exception:: HTTPVersionNotSupported

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   HTTP Version Not Supported

   .. attribute:: code
      :annotation: = 505

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Cannot fulfill request.

      


.. py:exception:: NetworkAuthenticationRequired

   Bases: :class:`pyre.http.exceptions.ProtocolError`

   Network Authentication Required

   .. attribute:: code
      :annotation: = 511

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = The client needs to authenticate to gain network access.

      


