---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 186ff32138bba0556b05e9674f1711e9425a20c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839265"
---
# <span data-ttu-id="efa97-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="efa97-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="efa97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efa97-102">SYNOPSIS</span></span>
<span data-ttu-id="efa97-103">Megkapja az adatbázis speciális veszélyforrások elleni védelemhez szükséges beállításait.</span><span class="sxs-lookup"><span data-stu-id="efa97-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="efa97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efa97-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSettings [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efa97-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="efa97-105">DESCRIPTION</span></span>
<span data-ttu-id="efa97-106">A **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** parancsmag az Azure SQL-adatbázisok speciális veszélyforrások elleni védelmét biztosító beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="efa97-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="efa97-107">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert annak az adatbázisnak a meghatározásához, amelyhez a parancsmag a beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="efa97-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="efa97-108">Példák</span><span class="sxs-lookup"><span data-stu-id="efa97-108">EXAMPLES</span></span>

### <span data-ttu-id="efa97-109">Példa 1: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="efa97-109">Example 1: Get the advanced threat protection settings for a database</span></span>
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

<span data-ttu-id="efa97-110">Ez a parancs a Database01 nevű adatbázis speciális fenyegetések elleni védelmét szolgáló beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="efa97-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="efa97-111">Az adatbázis a Server01 nevű kiszolgálón található, amelyet az erőforráscsoport ResourceGroup11 társítanak.</span><span class="sxs-lookup"><span data-stu-id="efa97-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="efa97-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efa97-112">PARAMETERS</span></span>

### <span data-ttu-id="efa97-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="efa97-113">-DatabaseName</span></span>
<span data-ttu-id="efa97-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efa97-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="efa97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa97-115">-DefaultProfile</span></span>
<span data-ttu-id="efa97-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="efa97-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efa97-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa97-117">-ResourceGroupName</span></span>
<span data-ttu-id="efa97-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="efa97-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="efa97-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="efa97-119">-ServerName</span></span>
<span data-ttu-id="efa97-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efa97-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="efa97-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="efa97-121">-Confirm</span></span>
<span data-ttu-id="efa97-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="efa97-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa97-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa97-123">-WhatIf</span></span>
<span data-ttu-id="efa97-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="efa97-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa97-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efa97-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa97-126">CommonParameters</span></span>
<span data-ttu-id="efa97-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efa97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa97-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa97-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa97-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa97-129">INPUTS</span></span>

### <span data-ttu-id="efa97-130">System. String</span><span class="sxs-lookup"><span data-stu-id="efa97-130">System.String</span></span>

## <span data-ttu-id="efa97-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa97-131">OUTPUTS</span></span>

### <span data-ttu-id="efa97-132">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="efa97-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="efa97-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efa97-133">NOTES</span></span>

## <span data-ttu-id="efa97-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efa97-134">RELATED LINKS</span></span>

[<span data-ttu-id="efa97-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="efa97-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)



