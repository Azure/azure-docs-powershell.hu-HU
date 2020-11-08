---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8090ee9cf6ec251668dbeadba6b18a7cde4898c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186696"
---
# <span data-ttu-id="92563-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="92563-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="92563-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92563-102">SYNOPSIS</span></span>
<span data-ttu-id="92563-103">Megkapja az adatbázis speciális veszélyforrások elleni védelemhez szükséges beállításait.</span><span class="sxs-lookup"><span data-stu-id="92563-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="92563-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92563-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92563-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92563-105">DESCRIPTION</span></span>
<span data-ttu-id="92563-106">A **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** parancsmag az Azure SQL-adatbázisok speciális veszélyforrások elleni védelmét biztosító beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="92563-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="92563-107">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert annak az adatbázisnak a meghatározásához, amelyhez a parancsmag a beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="92563-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="92563-108">Példák</span><span class="sxs-lookup"><span data-stu-id="92563-108">EXAMPLES</span></span>

### <span data-ttu-id="92563-109">Példa 1: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="92563-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="92563-110">Ez a parancs a Database01 nevű adatbázis speciális fenyegetések elleni védelmét szolgáló beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="92563-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="92563-111">Az adatbázis a Server01 nevű kiszolgálón található, amelyet az erőforráscsoport ResourceGroup11 társítanak.</span><span class="sxs-lookup"><span data-stu-id="92563-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="92563-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92563-112">PARAMETERS</span></span>

### <span data-ttu-id="92563-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="92563-113">-DatabaseName</span></span>
<span data-ttu-id="92563-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92563-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="92563-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92563-115">-DefaultProfile</span></span>
<span data-ttu-id="92563-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="92563-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92563-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92563-117">-ResourceGroupName</span></span>
<span data-ttu-id="92563-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="92563-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="92563-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="92563-119">-ServerName</span></span>
<span data-ttu-id="92563-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92563-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="92563-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92563-121">-Confirm</span></span>
<span data-ttu-id="92563-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92563-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92563-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92563-123">-WhatIf</span></span>
<span data-ttu-id="92563-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92563-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92563-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92563-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92563-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92563-126">CommonParameters</span></span>
<span data-ttu-id="92563-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92563-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92563-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="92563-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92563-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92563-129">INPUTS</span></span>

### <span data-ttu-id="92563-130">System. String</span><span class="sxs-lookup"><span data-stu-id="92563-130">System.String</span></span>

## <span data-ttu-id="92563-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92563-131">OUTPUTS</span></span>

### <span data-ttu-id="92563-132">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="92563-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="92563-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92563-133">NOTES</span></span>

## <span data-ttu-id="92563-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92563-134">RELATED LINKS</span></span>

[<span data-ttu-id="92563-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="92563-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



