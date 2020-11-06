---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494630"
---
# <span data-ttu-id="06fb1-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="06fb1-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="06fb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="06fb1-103">Egy adatbázis hosszú távú adatmegőrzési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="06fb1-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06fb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06fb1-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06fb1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="06fb1-106">A **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** parancsmag az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="06fb1-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="06fb1-107">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="06fb1-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="06fb1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="06fb1-108">EXAMPLES</span></span>

## <span data-ttu-id="06fb1-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06fb1-109">PARAMETERS</span></span>

### <span data-ttu-id="06fb1-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06fb1-110">-DatabaseName</span></span>
<span data-ttu-id="06fb1-111">Annak az SQL-adatbázisnak a neve, amelyhez a parancsmag házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="06fb1-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fb1-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06fb1-112">-ResourceGroupName</span></span>
<span data-ttu-id="06fb1-113">Az adatbázist tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06fb1-113">Specifies the name of the resource group that contains the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fb1-114">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="06fb1-114">-ServerName</span></span>
<span data-ttu-id="06fb1-115">Itt adhatja meg az adatbázist tároló kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="06fb1-115">Specifies the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fb1-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06fb1-116">-Confirm</span></span>
<span data-ttu-id="06fb1-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06fb1-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06fb1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06fb1-118">-WhatIf</span></span>
<span data-ttu-id="06fb1-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06fb1-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06fb1-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06fb1-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06fb1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fb1-121">-DefaultProfile</span></span>
<span data-ttu-id="06fb1-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06fb1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06fb1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fb1-123">CommonParameters</span></span>
<span data-ttu-id="06fb1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06fb1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fb1-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06fb1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fb1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06fb1-126">INPUTS</span></span>

## <span data-ttu-id="06fb1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06fb1-127">OUTPUTS</span></span>

## <span data-ttu-id="06fb1-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06fb1-128">NOTES</span></span>

## <span data-ttu-id="06fb1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06fb1-129">RELATED LINKS</span></span>

[<span data-ttu-id="06fb1-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="06fb1-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="06fb1-131">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="06fb1-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
