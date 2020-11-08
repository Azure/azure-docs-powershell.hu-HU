---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010785"
---
# <span data-ttu-id="7f07f-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="7f07f-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="7f07f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f07f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f07f-103">A kiszolgáló speciális veszélyforrások elleni védelemre vonatkozó beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7f07f-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="7f07f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f07f-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f07f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f07f-105">DESCRIPTION</span></span>
<span data-ttu-id="7f07f-106">A **Get-AzSqlServerAdvancedThreatProtectionSetting** parancsmag az Azure SQL Server speciális veszélyforrások elleni védelmét biztosító beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7f07f-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="7f07f-107">A parancsmag használatához adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert annak a kiszolgálónak a meghatározásához, amelynek a parancsmagja a beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="7f07f-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="7f07f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7f07f-108">EXAMPLES</span></span>

### <span data-ttu-id="7f07f-109">Példa 1: a speciális veszélyforrások elleni védelem beállításainak beszerzése egy kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="7f07f-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="7f07f-110">Ez a parancs a Server01 nevű kiszolgáló speciális veszélyforrásokkal kapcsolatos védelmi beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7f07f-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="7f07f-111">A kiszolgáló az erőforráscsoport ResourceGroup11 van társítva.</span><span class="sxs-lookup"><span data-stu-id="7f07f-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="7f07f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f07f-112">PARAMETERS</span></span>

### <span data-ttu-id="7f07f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f07f-113">-DefaultProfile</span></span>
<span data-ttu-id="7f07f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f07f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f07f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f07f-115">-ResourceGroupName</span></span>
<span data-ttu-id="7f07f-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="7f07f-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="7f07f-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7f07f-117">-ServerName</span></span>
<span data-ttu-id="7f07f-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f07f-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7f07f-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f07f-119">-Confirm</span></span>
<span data-ttu-id="7f07f-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f07f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f07f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f07f-121">-WhatIf</span></span>
<span data-ttu-id="7f07f-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f07f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f07f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f07f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f07f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f07f-124">CommonParameters</span></span>
<span data-ttu-id="7f07f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f07f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f07f-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7f07f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f07f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f07f-127">INPUTS</span></span>

### <span data-ttu-id="7f07f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7f07f-128">System.String</span></span>

## <span data-ttu-id="7f07f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f07f-129">OUTPUTS</span></span>

### <span data-ttu-id="7f07f-130">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="7f07f-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="7f07f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f07f-131">NOTES</span></span>

## <span data-ttu-id="7f07f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f07f-132">RELATED LINKS</span></span>

[<span data-ttu-id="7f07f-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="7f07f-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="7f07f-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7f07f-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


