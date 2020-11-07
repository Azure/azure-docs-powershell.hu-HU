---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 6cb14b368bf7f190c30ff32fdec12576d3189204
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669011"
---
# <span data-ttu-id="8b862-101">Get-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b862-101">Get-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="8b862-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b862-102">SYNOPSIS</span></span>
<span data-ttu-id="8b862-103">Az adatbázis veszélyforrás-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b862-103">Gets the threat detection policy for a database.</span></span>

## <span data-ttu-id="8b862-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b862-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b862-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b862-105">DESCRIPTION</span></span>
<span data-ttu-id="8b862-106">A **Get-AzSqlDatabaseThreatDetectionPolicy** parancsmag egy Azure SQL-adatbázis veszélyforrás-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b862-106">The **Get-AzSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="8b862-107">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert annak az adatbázisnak a meghatározásához, amelyhez a parancsmag a házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="8b862-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="8b862-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8b862-108">EXAMPLES</span></span>

### <span data-ttu-id="8b862-109">Példa 1: az adatbázis veszélyforrás-észlelési házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="8b862-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="8b862-110">Ez a parancs a Database01 nevű adatbázis fenyegetés-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b862-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="8b862-111">Az adatbázis a Server01 nevű kiszolgálón található, amelyet az erőforráscsoport ResourceGroup11 társítanak.</span><span class="sxs-lookup"><span data-stu-id="8b862-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="8b862-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b862-112">PARAMETERS</span></span>

### <span data-ttu-id="8b862-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8b862-113">-DatabaseName</span></span>
<span data-ttu-id="8b862-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b862-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="8b862-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b862-115">-DefaultProfile</span></span>
<span data-ttu-id="8b862-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8b862-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b862-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b862-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b862-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="8b862-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8b862-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8b862-119">-ServerName</span></span>
<span data-ttu-id="8b862-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b862-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="8b862-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b862-121">-Confirm</span></span>
<span data-ttu-id="8b862-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b862-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b862-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b862-123">-WhatIf</span></span>
<span data-ttu-id="8b862-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b862-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b862-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b862-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b862-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b862-126">CommonParameters</span></span>
<span data-ttu-id="8b862-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b862-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b862-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b862-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b862-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b862-129">INPUTS</span></span>

### <span data-ttu-id="8b862-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8b862-130">System.String</span></span>

## <span data-ttu-id="8b862-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b862-131">OUTPUTS</span></span>

### <span data-ttu-id="8b862-132">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8b862-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="8b862-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b862-133">NOTES</span></span>

## <span data-ttu-id="8b862-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b862-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b862-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b862-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)



