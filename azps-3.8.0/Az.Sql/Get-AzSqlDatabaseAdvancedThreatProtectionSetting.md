---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8090ee9cf6ec251668dbeadba6b18a7cde4898c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011566"
---
# <span data-ttu-id="52795-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="52795-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="52795-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52795-102">SYNOPSIS</span></span>
<span data-ttu-id="52795-103">Megkapja az adatbázis speciális veszélyforrások elleni védelemhez szükséges beállításait.</span><span class="sxs-lookup"><span data-stu-id="52795-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="52795-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52795-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52795-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="52795-105">DESCRIPTION</span></span>
<span data-ttu-id="52795-106">A **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** parancsmag az Azure SQL-adatbázisok speciális veszélyforrások elleni védelmét biztosító beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="52795-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="52795-107">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert annak az adatbázisnak a meghatározásához, amelyhez a parancsmag a beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="52795-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="52795-108">Példák</span><span class="sxs-lookup"><span data-stu-id="52795-108">EXAMPLES</span></span>

### <span data-ttu-id="52795-109">Példa 1: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="52795-109">Example 1: Get the advanced threat protection settings for a database</span></span>
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

<span data-ttu-id="52795-110">Ez a parancs a Database01 nevű adatbázis speciális fenyegetések elleni védelmét szolgáló beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="52795-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="52795-111">Az adatbázis a Server01 nevű kiszolgálón található, amelyet az erőforráscsoport ResourceGroup11 társítanak.</span><span class="sxs-lookup"><span data-stu-id="52795-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="52795-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52795-112">PARAMETERS</span></span>

### <span data-ttu-id="52795-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52795-113">-DatabaseName</span></span>
<span data-ttu-id="52795-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52795-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="52795-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52795-115">-DefaultProfile</span></span>
<span data-ttu-id="52795-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="52795-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52795-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52795-117">-ResourceGroupName</span></span>
<span data-ttu-id="52795-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="52795-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="52795-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="52795-119">-ServerName</span></span>
<span data-ttu-id="52795-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52795-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="52795-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52795-121">-Confirm</span></span>
<span data-ttu-id="52795-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52795-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52795-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52795-123">-WhatIf</span></span>
<span data-ttu-id="52795-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52795-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52795-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52795-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52795-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52795-126">CommonParameters</span></span>
<span data-ttu-id="52795-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52795-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52795-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="52795-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52795-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52795-129">INPUTS</span></span>

### <span data-ttu-id="52795-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52795-130">System.String</span></span>

## <span data-ttu-id="52795-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52795-131">OUTPUTS</span></span>

### <span data-ttu-id="52795-132">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="52795-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="52795-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52795-133">NOTES</span></span>

## <span data-ttu-id="52795-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52795-134">RELATED LINKS</span></span>

[<span data-ttu-id="52795-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="52795-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



