---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 490f7b4a0cb723d02deb1d18e8a2ddfb993e7f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011677"
---
# <span data-ttu-id="1ec01-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ec01-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="1ec01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ec01-102">SYNOPSIS</span></span>

## <span data-ttu-id="1ec01-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ec01-103">SYNTAX</span></span>

### <span data-ttu-id="1ec01-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1ec01-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="1ec01-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1ec01-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="1ec01-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ec01-106">DESCRIPTION</span></span>
<span data-ttu-id="1ec01-107">A **Edit-AzWebAppBackupConfiguration** parancsmag az Azure Web App jelenlegi biztonsági biztonsági másolatát szerkeszti.</span><span class="sxs-lookup"><span data-stu-id="1ec01-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="1ec01-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1ec01-108">EXAMPLES</span></span>

## <span data-ttu-id="1ec01-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ec01-109">PARAMETERS</span></span>

### <span data-ttu-id="1ec01-110">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="1ec01-110">-Databases</span></span>
<span data-ttu-id="1ec01-111">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="1ec01-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec01-112">-DefaultProfile</span></span>
<span data-ttu-id="1ec01-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ec01-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ec01-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="1ec01-114">-FrequencyInterval</span></span>
<span data-ttu-id="1ec01-115">Gyakorisági intervallum</span><span class="sxs-lookup"><span data-stu-id="1ec01-115">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="1ec01-116">-FrequencyUnit</span></span>
<span data-ttu-id="1ec01-117">Frekvencia egység</span><span class="sxs-lookup"><span data-stu-id="1ec01-117">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="1ec01-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="1ec01-119">Legalább egy biztonsági mentési beállítás megtartása</span><span class="sxs-lookup"><span data-stu-id="1ec01-119">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ec01-120">-Name</span></span>
<span data-ttu-id="1ec01-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="1ec01-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec01-122">-ResourceGroupName</span></span>
<span data-ttu-id="1ec01-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1ec01-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1ec01-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="1ec01-125">Megőrzési időszak napokban</span><span class="sxs-lookup"><span data-stu-id="1ec01-125">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="1ec01-126">-Slot</span></span>
<span data-ttu-id="1ec01-127">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="1ec01-127">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-128">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="1ec01-128">-StartTime</span></span>
<span data-ttu-id="1ec01-129">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="1ec01-129">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="1ec01-130">-StorageAccountUrl</span></span>
<span data-ttu-id="1ec01-131">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="1ec01-131">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1ec01-132">-WebApp</span></span>
<span data-ttu-id="1ec01-133">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="1ec01-133">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec01-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec01-134">CommonParameters</span></span>
<span data-ttu-id="1ec01-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ec01-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec01-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec01-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec01-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ec01-137">INPUTS</span></span>

### <span data-ttu-id="1ec01-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1ec01-138">System.Int32</span></span>

### <span data-ttu-id="1ec01-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1ec01-139">System.String</span></span>

### <span data-ttu-id="1ec01-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="1ec01-140">System.DateTime</span></span>

### <span data-ttu-id="1ec01-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ec01-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1ec01-142">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1ec01-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="1ec01-143">Microsoft. Azure. Management. WebSites. models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="1ec01-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="1ec01-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ec01-144">OUTPUTS</span></span>

### <span data-ttu-id="1ec01-145">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ec01-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="1ec01-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ec01-146">NOTES</span></span>

## <span data-ttu-id="1ec01-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ec01-147">RELATED LINKS</span></span>

[<span data-ttu-id="1ec01-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ec01-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


