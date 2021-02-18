---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 85a45c1a5f7c4d88adaf4e9b9da35b415b7a2093
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405805"
---
# <span data-ttu-id="be27d-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="be27d-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="be27d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be27d-102">SYNOPSIS</span></span>
<span data-ttu-id="be27d-103">A komplex veszélyforrások elleni védelem speciális beállításainak lekérdezése egy adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="be27d-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="be27d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="be27d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSettings [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be27d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="be27d-105">DESCRIPTION</span></span>
<span data-ttu-id="be27d-106">A **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** parancsmag megkapja egy Azure SQL-adatbázis komplex veszélyforrás-védelmi beállításait.</span><span class="sxs-lookup"><span data-stu-id="be27d-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="be27d-107">A parancsmagot úgy használhatja, hogy megadja a *ResourceGroupName,* *a ServerName* és a *DatabaseName* paramétert annak az adatbázisnak a azonosításához, amelyhez ez a parancsmag a beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="be27d-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="be27d-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="be27d-108">EXAMPLES</span></span>

### <span data-ttu-id="be27d-109">1. példa: A komplex veszélyforrások elleni védelem speciális beállításainak lekérte</span><span class="sxs-lookup"><span data-stu-id="be27d-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="be27d-110">Ez a parancs a Database01 nevű adatbázis komplex veszélyforrás-védelmi beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="be27d-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="be27d-111">Az adatbázis a Server01 nevű kiszolgálón található, amely az ResourceGroup11 erőforráscsoporthoz van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="be27d-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="be27d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be27d-112">PARAMETERS</span></span>

### <span data-ttu-id="be27d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="be27d-113">-DatabaseName</span></span>
<span data-ttu-id="be27d-114">Egy adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be27d-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="be27d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be27d-115">-DefaultProfile</span></span>
<span data-ttu-id="be27d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="be27d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be27d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be27d-117">-ResourceGroupName</span></span>
<span data-ttu-id="be27d-118">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="be27d-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="be27d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="be27d-119">-ServerName</span></span>
<span data-ttu-id="be27d-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be27d-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="be27d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be27d-121">-Confirm</span></span>
<span data-ttu-id="be27d-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="be27d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be27d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be27d-123">-WhatIf</span></span>
<span data-ttu-id="be27d-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="be27d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be27d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be27d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be27d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be27d-126">CommonParameters</span></span>
<span data-ttu-id="be27d-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be27d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be27d-128">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be27d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be27d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be27d-129">INPUTS</span></span>

### <span data-ttu-id="be27d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="be27d-130">System.String</span></span>

## <span data-ttu-id="be27d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be27d-131">OUTPUTS</span></span>

### <span data-ttu-id="be27d-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="be27d-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="be27d-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="be27d-133">NOTES</span></span>

## <span data-ttu-id="be27d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be27d-134">RELATED LINKS</span></span>




