---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/edit-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: cfac8f1cd3d25ff630900bb5d7723e713b3d4c65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842818"
---
# <span data-ttu-id="fea82-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="fea82-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="fea82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fea82-102">SYNOPSIS</span></span>

## <span data-ttu-id="fea82-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fea82-103">SYNTAX</span></span>

### <span data-ttu-id="fea82-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fea82-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="fea82-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fea82-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="fea82-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="fea82-106">DESCRIPTION</span></span>
<span data-ttu-id="fea82-107">A **Edit-AzWebAppBackupConfiguration** parancsmag az Azure Web App jelenlegi biztonsági biztonsági másolatát szerkeszti.</span><span class="sxs-lookup"><span data-stu-id="fea82-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="fea82-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fea82-108">EXAMPLES</span></span>

## <span data-ttu-id="fea82-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fea82-109">PARAMETERS</span></span>

### <span data-ttu-id="fea82-110">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="fea82-110">-Databases</span></span>
<span data-ttu-id="fea82-111">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="fea82-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea82-112">-DefaultProfile</span></span>
<span data-ttu-id="fea82-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fea82-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="fea82-114">-FrequencyInterval</span></span>
<span data-ttu-id="fea82-115">Gyakorisági intervallum</span><span class="sxs-lookup"><span data-stu-id="fea82-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="fea82-116">-FrequencyUnit</span></span>
<span data-ttu-id="fea82-117">Frekvencia egység</span><span class="sxs-lookup"><span data-stu-id="fea82-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="fea82-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="fea82-119">Legalább egy biztonsági mentési beállítás megtartása</span><span class="sxs-lookup"><span data-stu-id="fea82-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fea82-120">-Name</span></span>
<span data-ttu-id="fea82-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="fea82-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea82-122">-ResourceGroupName</span></span>
<span data-ttu-id="fea82-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="fea82-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="fea82-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="fea82-125">Megőrzési időszak napokban</span><span class="sxs-lookup"><span data-stu-id="fea82-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="fea82-126">-Slot</span></span>
<span data-ttu-id="fea82-127">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="fea82-127">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-128">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="fea82-128">-StartTime</span></span>
<span data-ttu-id="fea82-129">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="fea82-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="fea82-130">-StorageAccountUrl</span></span>
<span data-ttu-id="fea82-131">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="fea82-131">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fea82-132">-WebApp</span></span>
<span data-ttu-id="fea82-133">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="fea82-133">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea82-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea82-134">CommonParameters</span></span>
<span data-ttu-id="fea82-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fea82-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea82-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea82-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea82-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea82-137">INPUTS</span></span>

### <span data-ttu-id="fea82-138">Webhely</span><span class="sxs-lookup"><span data-stu-id="fea82-138">Site</span></span>
<span data-ttu-id="fea82-139">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fea82-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fea82-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea82-140">OUTPUTS</span></span>

### <span data-ttu-id="fea82-141">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="fea82-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="fea82-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fea82-142">NOTES</span></span>

## <span data-ttu-id="fea82-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fea82-143">RELATED LINKS</span></span>

[<span data-ttu-id="fea82-144">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="fea82-144">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


