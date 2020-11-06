---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 5136da99879e4636018ae1a01cc95f39f2924b4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498767"
---
# <span data-ttu-id="c6df4-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c6df4-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="c6df4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6df4-102">SYNOPSIS</span></span>
<span data-ttu-id="c6df4-103">Az adatbázis TDE állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c6df4-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6df4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6df4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6df4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6df4-105">DESCRIPTION</span></span>
<span data-ttu-id="c6df4-106">A **Get-AzureRmSqlDatabaseTransparentDataEncryption** parancsmag az Azure SQL-adatbázisok átlátszó adattitkosításának (TDE) állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="c6df4-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="c6df4-107">További információért olvassa el az átlátszó adattitkosítás az Azure SQL-adatbázisokkal https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) a Microsoft Developer Network Library-ban című témakört).</span><span class="sxs-lookup"><span data-stu-id="c6df4-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="c6df4-108">Ez a parancsmag a TDE jelenlegi állapotát kapja meg, de a titkosítás és a visszafejtés egyaránt hosszú műveleteket végezhet.</span><span class="sxs-lookup"><span data-stu-id="c6df4-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="c6df4-109">A titkosítási vizsgálat előrehaladásának megtekintéséhez futtassa az Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c6df4-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>

<span data-ttu-id="c6df4-110">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="c6df4-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c6df4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c6df4-111">EXAMPLES</span></span>

### <span data-ttu-id="c6df4-112">Példa 1: TDE állapotának beszerzése egy adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="c6df4-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="c6df4-113">Ez a parancs a server01 nevű kiszolgálón a Database01 nevű adatbázis TDE állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c6df4-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="c6df4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6df4-114">PARAMETERS</span></span>

### <span data-ttu-id="c6df4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6df4-115">-DatabaseName</span></span>
<span data-ttu-id="c6df4-116">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja a TDE állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="c6df4-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6df4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6df4-117">-DefaultProfile</span></span>
<span data-ttu-id="c6df4-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c6df4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6df4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6df4-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6df4-120">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c6df4-120">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6df4-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c6df4-121">-ServerName</span></span>
<span data-ttu-id="c6df4-122">Itt adhatja meg annak az adatbázisnak a nevét, amelynek a parancsmagja a TDE állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="c6df4-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6df4-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6df4-123">-Confirm</span></span>
<span data-ttu-id="c6df4-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6df4-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6df4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6df4-125">-WhatIf</span></span>
<span data-ttu-id="c6df4-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6df4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6df4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6df4-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6df4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6df4-128">CommonParameters</span></span>
<span data-ttu-id="c6df4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6df4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6df4-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6df4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6df4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6df4-131">INPUTS</span></span>

### <span data-ttu-id="c6df4-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="c6df4-132">None</span></span>
<span data-ttu-id="c6df4-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c6df4-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6df4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6df4-134">OUTPUTS</span></span>

### <span data-ttu-id="c6df4-135">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="c6df4-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="c6df4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6df4-136">NOTES</span></span>

## <span data-ttu-id="c6df4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6df4-137">RELATED LINKS</span></span>

[<span data-ttu-id="c6df4-138">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="c6df4-138">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="c6df4-139">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c6df4-139">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)
