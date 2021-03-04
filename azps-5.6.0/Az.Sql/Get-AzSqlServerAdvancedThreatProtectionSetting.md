---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 705412a560c4d4c0734e8e81a07fb2a85224f8c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928481"
---
# <span data-ttu-id="782e4-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="782e4-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="782e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="782e4-102">SYNOPSIS</span></span>
<span data-ttu-id="782e4-103">A kiszolgáló komplex veszélyforrások elleni védelemre vonatkozó speciális beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="782e4-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="782e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="782e4-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="782e4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="782e4-105">DESCRIPTION</span></span>
<span data-ttu-id="782e4-106">A **Get-AzSqlServerAdvancedThreatProtectionSetting** parancsmag megkapja egy Azure SQL-kiszolgáló komplex veszélyforrás-védelmi beállításait.</span><span class="sxs-lookup"><span data-stu-id="782e4-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="782e4-107">A parancsmagot úgy használhatja, hogy megadja a *ResourceGroupName* és *a ServerName* paramétert annak a kiszolgálónak a azonosításához, amelynek a parancsmagja megkapja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="782e4-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="782e4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="782e4-108">EXAMPLES</span></span>

### <span data-ttu-id="782e4-109">1. példa: A komplex veszélyforrások elleni védelem speciális beállításainak lekérte egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="782e4-109">Example 1: Get the advanced threat protection settings for a server</span></span>
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

<span data-ttu-id="782e4-110">Ez a parancs a Kiszolgáló01 nevű kiszolgáló komplex veszélyforrás-védelmi beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="782e4-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="782e4-111">A kiszolgáló hozzá van rendelve az Erőforráscsoport11 erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="782e4-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="782e4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="782e4-112">PARAMETERS</span></span>

### <span data-ttu-id="782e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782e4-113">-DefaultProfile</span></span>
<span data-ttu-id="782e4-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="782e4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="782e4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782e4-115">-ResourceGroupName</span></span>
<span data-ttu-id="782e4-116">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="782e4-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="782e4-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="782e4-117">-ServerName</span></span>
<span data-ttu-id="782e4-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="782e4-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="782e4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="782e4-119">-Confirm</span></span>
<span data-ttu-id="782e4-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="782e4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="782e4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="782e4-121">-WhatIf</span></span>
<span data-ttu-id="782e4-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="782e4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="782e4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="782e4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="782e4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782e4-124">CommonParameters</span></span>
<span data-ttu-id="782e4-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782e4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782e4-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="782e4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782e4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="782e4-127">INPUTS</span></span>

### <span data-ttu-id="782e4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="782e4-128">System.String</span></span>

## <span data-ttu-id="782e4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="782e4-129">OUTPUTS</span></span>

### <span data-ttu-id="782e4-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="782e4-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="782e4-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="782e4-131">NOTES</span></span>

## <span data-ttu-id="782e4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="782e4-132">RELATED LINKS</span></span>

[<span data-ttu-id="782e4-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="782e4-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="782e4-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="782e4-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


