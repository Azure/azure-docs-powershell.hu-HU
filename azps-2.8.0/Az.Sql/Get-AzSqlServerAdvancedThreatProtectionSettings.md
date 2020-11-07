---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 1895fe45f51782cc1a3a54d8b2d0f2da752c2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839174"
---
# <span data-ttu-id="3e75e-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="3e75e-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="3e75e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e75e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e75e-103">A kiszolgáló speciális veszélyforrások elleni védelemre vonatkozó beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3e75e-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="3e75e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e75e-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSettings -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e75e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e75e-105">DESCRIPTION</span></span>
<span data-ttu-id="3e75e-106">A **Get-AzSqlServerAdvancedThreatProtectionSettings** parancsmag az Azure SQL Server speciális veszélyforrások elleni védelmét biztosító beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3e75e-106">The **Get-AzSqlServerAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="3e75e-107">A parancsmag használatához adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert annak a kiszolgálónak a meghatározásához, amelynek a parancsmagja a beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="3e75e-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="3e75e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3e75e-108">EXAMPLES</span></span>

### <span data-ttu-id="3e75e-109">Példa 1: a speciális veszélyforrások elleni védelem beállításainak beszerzése egy kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="3e75e-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="3e75e-110">Ez a parancs a Server01 nevű kiszolgáló speciális veszélyforrásokkal kapcsolatos védelmi beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3e75e-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="3e75e-111">A kiszolgáló az erőforráscsoport ResourceGroup11 van társítva.</span><span class="sxs-lookup"><span data-stu-id="3e75e-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="3e75e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e75e-112">PARAMETERS</span></span>

### <span data-ttu-id="3e75e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e75e-113">-DefaultProfile</span></span>
<span data-ttu-id="3e75e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3e75e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e75e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e75e-115">-ResourceGroupName</span></span>
<span data-ttu-id="3e75e-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="3e75e-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="3e75e-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3e75e-117">-ServerName</span></span>
<span data-ttu-id="3e75e-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e75e-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3e75e-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e75e-119">-Confirm</span></span>
<span data-ttu-id="3e75e-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e75e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e75e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e75e-121">-WhatIf</span></span>
<span data-ttu-id="3e75e-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e75e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e75e-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e75e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e75e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e75e-124">CommonParameters</span></span>
<span data-ttu-id="3e75e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e75e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e75e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e75e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e75e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e75e-127">INPUTS</span></span>

### <span data-ttu-id="3e75e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3e75e-128">System.String</span></span>

## <span data-ttu-id="3e75e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e75e-129">OUTPUTS</span></span>

### <span data-ttu-id="3e75e-130">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="3e75e-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="3e75e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e75e-131">NOTES</span></span>

## <span data-ttu-id="3e75e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e75e-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e75e-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="3e75e-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)

[<span data-ttu-id="3e75e-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3e75e-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


