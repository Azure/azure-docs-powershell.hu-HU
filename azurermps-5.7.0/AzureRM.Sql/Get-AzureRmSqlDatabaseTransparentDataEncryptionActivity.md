---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: ec7c452939d82b82deed507c667bdc9cdeab3cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498760"
---
# <span data-ttu-id="5d835-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="5d835-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="5d835-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d835-102">SYNOPSIS</span></span>
<span data-ttu-id="5d835-103">Egy adatbázis TDE-vizsgálatának előrehaladását kapja.</span><span class="sxs-lookup"><span data-stu-id="5d835-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d835-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d835-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d835-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d835-105">DESCRIPTION</span></span>
<span data-ttu-id="5d835-106">A **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** parancsmag az Azure SQL-adatbázisok átlátszó adattitkosítási (TDE) vizsgálatának előrehaladását kapja.</span><span class="sxs-lookup"><span data-stu-id="5d835-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="5d835-107">Ha nem fut a titkosítási tartomány, ez a parancsmag üres listát ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5d835-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="5d835-108">További információért olvassa el az átlátszó adattitkosítás az Azure SQL-adatbázisokkal https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) a Microsoft Developer Network Library-ban című témakört).</span><span class="sxs-lookup"><span data-stu-id="5d835-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="5d835-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="5d835-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5d835-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5d835-110">EXAMPLES</span></span>

### <span data-ttu-id="5d835-111">1. példa: TDE-tevékenység beszerzése egy adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="5d835-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="5d835-112">Ez a parancs a server01 nevű kiszolgálón a database01 nevű adatbázis TDE tevékenységét kapja.</span><span class="sxs-lookup"><span data-stu-id="5d835-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="5d835-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d835-113">PARAMETERS</span></span>

### <span data-ttu-id="5d835-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d835-114">-DatabaseName</span></span>
<span data-ttu-id="5d835-115">Annak az adatbázisnak a neve, amelyhez a parancsmag TDE-titkosítási tevékenységet kap.</span><span class="sxs-lookup"><span data-stu-id="5d835-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="5d835-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d835-116">-DefaultProfile</span></span>
<span data-ttu-id="5d835-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5d835-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d835-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d835-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d835-119">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5d835-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5d835-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5d835-120">-ServerName</span></span>
<span data-ttu-id="5d835-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d835-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5d835-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d835-122">-Confirm</span></span>
<span data-ttu-id="5d835-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d835-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d835-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d835-124">-WhatIf</span></span>
<span data-ttu-id="5d835-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d835-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d835-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d835-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d835-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d835-127">CommonParameters</span></span>
<span data-ttu-id="5d835-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d835-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d835-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d835-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d835-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d835-130">INPUTS</span></span>

### <span data-ttu-id="5d835-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d835-131">None</span></span>
<span data-ttu-id="5d835-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5d835-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d835-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d835-133">OUTPUTS</span></span>

### <span data-ttu-id="5d835-134">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="5d835-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="5d835-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d835-135">NOTES</span></span>

## <span data-ttu-id="5d835-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d835-136">RELATED LINKS</span></span>

[<span data-ttu-id="5d835-137">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5d835-137">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="5d835-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5d835-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


