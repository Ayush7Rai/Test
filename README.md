# Test
-- Insert into user table
INSERT INTO user (user_id, username, name, email, role) VALUES
(1, 'bob', 'Bob Smith', 'bob.smith@example.com', 'Director'),
(2, 'charlie', 'Charlie Brown', 'charlie.brown@example.com', 'Manager'),
(3, 'david', 'David Wilson', 'david.wilson@example.com', 'Associate'),
(4, 'eva', 'Eva Davis', 'eva.davis@example.com', 'Analyst'),
(5, 'frank', 'Frank Moore', 'frank.moore@example.com', 'Trader');

-- Insert into book table
INSERT INTO book (book_id, name) VALUES
(1, 'CX9'),
(2, 'FX2'),
(3, 'EU5'),
(4, 'JP7'),
(5, 'BA1');

-- Insert into security table
INSERT INTO security (security_id, isin, cusip, maturity_date, issuer_name, type, coupon, face_value, currency, status) VALUES
(1, 'ISIN000001', 'CUSIP000001', '2029-11-21', 'US Treasury', 'Municipal Bond', 3.11, 4248, 'GBP', 'active'),
(2, 'ISIN000002', 'CUSIP000002', '2029-09-12', 'General Electric', 'Municipal Bond', 2.66, 4886, 'JPY', 'active'),
(3, 'ISIN000003', 'CUSIP000003', '2025-08-29', 'ExxonMobil', 'Municipal Bond', 2.29, 1594, 'GBP', 'active'),
(4, 'ISIN000004', 'CUSIP000004', '2028-12-23', 'ExxonMobil', 'Corporate Bond', 3.47, 1415, 'EUR', 'active'),
(5, 'ISIN000005', 'CUSIP000005', '2028-04-18', 'Apple Inc.', 'Zero-Coupon Bond', 0.7, 4909, 'EUR', 'active'),
(6, 'ISIN000006', 'CUSIP000006', '2027-05-11', 'General Electric', 'Corporate Bond', 2.92, 3487, 'GBP', 'active'),
(7, 'ISIN000007', 'CUSIP000007', '2027-04-16', 'Microsoft Corp.', 'Corporate Bond', 2.82, 1430, 'EUR', 'active'),
(8, 'ISIN000008', 'CUSIP000008', '2028-05-17', 'Microsoft Corp.', 'Corporate Bond', 1.12, 593, 'GBP', 'active'),
(9, 'ISIN000009', 'CUSIP000009', '2025-10-21', 'US Treasury', 'Government Bond', 3.47, 1561, 'USD', 'active'),
(10, 'ISIN000010', 'CUSIP000010', '2026-09-14', 'General Electric', 'Convertible Bond', 3.73, 2465, 'JPY', 'active');

-- Insert into counterparty table
INSERT INTO counterparty (counterparty_id, name) VALUES
(1, 'JP Morgan'),
(2, 'Morgan Stanley'),
(3, 'Barclays'),
(4, 'Citibank'),
(5, 'Goldman Sachs');

-- Insert into trade table
INSERT INTO trade (trade_id, book_id, security_id, counterparty_id, quantity, unit_price, currency, buy_sell_indicator, trade_date, settlement_date, assigned_user_status, assigned_user_id) VALUES
(1, 3, 4, 5, 189, 106.37, 'GBP', 'sell', '2024-06-30', '2024-08-06', TRUE, 4),
(2, 3, 6, 1, 435, 107.36, 'JPY', 'buy', '2024-05-05', '2024-08-30', TRUE, 5),
(3, 2, 7, 2, 335, 92.64, 'GBP', 'sell', '2023-11-13', '2024-08-07', TRUE, 3),
(4, 2, 6, 3, 242, 108.16, 'GBP', 'buy', '2024-05-29', '2024-08-23', FALSE, 2),
(5, 2, 10, 4, 437, 108.55, 'USD', 'sell', '2023-09-03', '2024-08-08', FALSE, 5),
(6, 5, 5, 1, 369, 90.39, 'USD', 'sell', '2024-07-14', '2024-08-28', FALSE, 4),
(7, 2, 1, 2, 15, 107.87, 'USD', 'buy', '2024-06-20', '2024-09-01', FALSE, 5),
(8, 1, 1, 3, 65, 92.62, 'EUR', 'sell', '2023-10-16', '2024-08-04', FALSE, 3),
(9, 5, 1, 4, 468, 103.54, 'GBP', 'buy', '2023-11-28', '2024-08-06', TRUE, 4),
(10, 5, 1, 5, 212, 94.76, 'GBP', 'buy', '2023-12-21', '2024-08-16', FALSE, 5);

-- Insert into book_user table
INSERT INTO book_user (book_user_id, book_id, user_id) VALUES
(1, 1, 1),
(2, 1, 3),
(3, 4, 4),
(4, 4, 4),
(5, 3, 2),
(6, 1, 1),
(7, 5, 1),
(8, 5, 5),
(9, 3, 4),
(10, 5, 4);
