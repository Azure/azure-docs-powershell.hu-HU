---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: f8d01165825c63ece34779f58cb94a3f8e0af40c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668932"
---
# <span data-ttu-id="3af9b-101">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3af9b-101">Get-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="3af9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3af9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3af9b-103">A kiszolgáló veszélyforrás-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3af9b-103">Gets the threat detection policy for a server.</span></span>

## <span data-ttu-id="3af9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3af9b-104">SYNTAX</span></span>

```
Get-AzSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af9b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3af9b-105">DESCRIPTION</span></span>
<span data-ttu-id="3af9b-106">A **Get-AzSqlServerThreatDetectionPolicy** parancsmag az Azure SQL Server fenyegetések észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3af9b-106">The **Get-AzSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="3af9b-107">A parancsmag használatához adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert annak a kiszolgálónak a meghatározásához, amelynek a parancsmagja a házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="3af9b-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="3af9b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3af9b-108">EXAMPLES</span></span>

### <span data-ttu-id="3af9b-109">Példa 1: a fenyegetések észlelési házirendjének beszerzése egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="3af9b-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="3af9b-110">Ez a parancs a Server01 nevű kiszolgáló fenyegetés-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3af9b-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="3af9b-111">A kiszolgáló az erőforráscsoport ResourceGroup11 van társítva.</span><span class="sxs-lookup"><span data-stu-id="3af9b-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="3af9b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3af9b-112">PARAMETERS</span></span>

### <span data-ttu-id="3af9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af9b-113">-DefaultProfile</span></span>
<span data-ttu-id="3af9b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3af9b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3af9b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af9b-115">-ResourceGroupName</span></span>
<span data-ttu-id="3af9b-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="3af9b-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="3af9b-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3af9b-117">-ServerName</span></span>
<span data-ttu-id="3af9b-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3af9b-118">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af9b-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3af9b-119">-Confirm</span></span>
<span data-ttu-id="3af9b-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3af9b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af9b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af9b-121">-WhatIf</span></span>
<span data-ttu-id="3af9b-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3af9b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af9b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3af9b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af9b-124">CommonParameters</span></span>
<span data-ttu-id="3af9b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3af9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af9b-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3af9b-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af9b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3af9b-127">INPUTS</span></span>

### <span data-ttu-id="3af9b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3af9b-128">System.String</span></span>

## <span data-ttu-id="3af9b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3af9b-129">OUTPUTS</span></span>

### <span data-ttu-id="3af9b-130">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3af9b-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="3af9b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3af9b-131">NOTES</span></span>

## <span data-ttu-id="3af9b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3af9b-132">RELATED LINKS</span></span>

[<span data-ttu-id="3af9b-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3af9b-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="3af9b-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3af9b-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


