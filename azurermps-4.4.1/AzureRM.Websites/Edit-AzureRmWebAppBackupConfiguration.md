---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: d7fd26d81b683095fb08c1dbca3226761f047d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494593"
---
# <span data-ttu-id="f1e21-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1e21-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f1e21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1e21-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1e21-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1e21-103">SYNTAX</span></span>

### <span data-ttu-id="f1e21-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f1e21-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="f1e21-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f1e21-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="f1e21-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1e21-106">DESCRIPTION</span></span>
<span data-ttu-id="f1e21-107">A **Edit-AzureRmWebAppBackupConfiguration** parancsmag az Azure Web App jelenlegi biztonsági biztonsági másolatát szerkeszti.</span><span class="sxs-lookup"><span data-stu-id="f1e21-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="f1e21-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f1e21-108">EXAMPLES</span></span>

## <span data-ttu-id="f1e21-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1e21-109">PARAMETERS</span></span>

### <span data-ttu-id="f1e21-110">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="f1e21-110">-Databases</span></span>
<span data-ttu-id="f1e21-111">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="f1e21-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="f1e21-112">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="f1e21-112">-FrequencyInterval</span></span>
<span data-ttu-id="f1e21-113">Gyakorisági intervallum</span><span class="sxs-lookup"><span data-stu-id="f1e21-113">Frequency Interval</span></span>

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

### <span data-ttu-id="f1e21-114">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="f1e21-114">-FrequencyUnit</span></span>
<span data-ttu-id="f1e21-115">Frekvencia egység</span><span class="sxs-lookup"><span data-stu-id="f1e21-115">Frequency Unit</span></span>

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

### <span data-ttu-id="f1e21-116">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="f1e21-116">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="f1e21-117">Legalább egy biztonsági mentési beállítás megtartása</span><span class="sxs-lookup"><span data-stu-id="f1e21-117">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="f1e21-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1e21-118">-Name</span></span>
<span data-ttu-id="f1e21-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f1e21-119">WebApp Name</span></span>

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

### <span data-ttu-id="f1e21-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e21-120">-ResourceGroupName</span></span>
<span data-ttu-id="f1e21-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f1e21-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f1e21-122">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f1e21-122">-RetentionPeriodInDays</span></span>
<span data-ttu-id="f1e21-123">Megőrzési időszak napokban</span><span class="sxs-lookup"><span data-stu-id="f1e21-123">Retention Period In Days</span></span>

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

### <span data-ttu-id="f1e21-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="f1e21-124">-Slot</span></span>
<span data-ttu-id="f1e21-125">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="f1e21-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f1e21-126">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="f1e21-126">-StartTime</span></span>
<span data-ttu-id="f1e21-127">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="f1e21-127">StartTime in UTC</span></span>

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

### <span data-ttu-id="f1e21-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f1e21-128">-StorageAccountUrl</span></span>
<span data-ttu-id="f1e21-129">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="f1e21-129">Storage Account Url</span></span>

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

### <span data-ttu-id="f1e21-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f1e21-130">-WebApp</span></span>
<span data-ttu-id="f1e21-131">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="f1e21-131">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e21-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e21-132">-DefaultProfile</span></span>
<span data-ttu-id="f1e21-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1e21-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e21-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e21-134">CommonParameters</span></span>
<span data-ttu-id="f1e21-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1e21-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e21-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e21-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e21-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e21-137">INPUTS</span></span>

### <span data-ttu-id="f1e21-138">Webhely</span><span class="sxs-lookup"><span data-stu-id="f1e21-138">Site</span></span>
<span data-ttu-id="f1e21-139">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f1e21-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f1e21-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e21-140">OUTPUTS</span></span>

### <span data-ttu-id="f1e21-141">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1e21-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f1e21-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1e21-142">NOTES</span></span>

## <span data-ttu-id="f1e21-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1e21-143">RELATED LINKS</span></span>

[<span data-ttu-id="f1e21-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1e21-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


