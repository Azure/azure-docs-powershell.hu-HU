---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015776"
---
# <span data-ttu-id="e6487-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e6487-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="e6487-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6487-102">SYNOPSIS</span></span>
<span data-ttu-id="e6487-103">A kötet-tároló csoportok feladatátvételi műveletét kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="e6487-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="e6487-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6487-104">SYNTAX</span></span>

### <span data-ttu-id="e6487-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6487-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6487-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="e6487-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6487-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="e6487-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6487-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6487-108">DESCRIPTION</span></span>
<span data-ttu-id="e6487-109">A **Start-AzureStorSimpleDeviceFailoverJob** parancsmag egy vagy több mennyiségi tároló csoport feladatátvételi műveletét kezdeményezi egyik eszközről a másikra.</span><span class="sxs-lookup"><span data-stu-id="e6487-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="e6487-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e6487-110">EXAMPLES</span></span>

### <span data-ttu-id="e6487-111">1. példa: feladatátvételi feladat indítása névvel ellátott eszközön és elnevezett céleszköz</span><span class="sxs-lookup"><span data-stu-id="e6487-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="e6487-112">Ez a parancs a **Get-AzureStorSimpleFailoverVolumeContainers** parancsmag használatával kapja meg a ChewD_App7 nevű eszköz feladatátvevő mennyiségi tárolóit.</span><span class="sxs-lookup"><span data-stu-id="e6487-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="e6487-113">A parancs átadja az eredményeket a **Where-Object** parancsmagnak, amely a **IsDCGroupEligibleForDR** tulajdonságtól $True eltérő értéket tartalmazó tárolókat visz le.</span><span class="sxs-lookup"><span data-stu-id="e6487-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="e6487-114">További információért írja be a következőt: `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="e6487-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="e6487-115">Az aktuális parancsmag feladatátvételi feladatokat indít a fennmaradó feladatátvevő mennyiségi tárolókban.</span><span class="sxs-lookup"><span data-stu-id="e6487-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="e6487-116">A parancs az eszköz nevét és a céleszköz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6487-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="e6487-117">A parancs a parancsmag által elindított feladat példányának AZONOSÍTÓját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e6487-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="e6487-118">2. példa: feladatátvételi feladat indítása eszközhöz és az AZONOSÍTÓval megadott céleszköz</span><span class="sxs-lookup"><span data-stu-id="e6487-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="e6487-119">Ez a parancs a **Get-AzureStorSimpleFailoverVolumeContainers** használatával megkapja a ChewD_App7 nevű eszköz feladatátvevő mennyiségi tárolóit.</span><span class="sxs-lookup"><span data-stu-id="e6487-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="e6487-120">A parancs a találatokat a **Where-Object** értékre adja át, amely a **IsDCGroupEligibleForDR** tulajdonságtól eltérő értékkel rendelkező $Trueokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e6487-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="e6487-121">A parancsmag átadja az eredményeket a **Select-Object** parancsmagnak, amely kijelöli az első objektumot, amelyet az aktuális parancsmagnak szeretne továbbítani.</span><span class="sxs-lookup"><span data-stu-id="e6487-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="e6487-122">További információért írja be a következőt: `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="e6487-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="e6487-123">Az aktuális parancsmag a kijelölt feladatátvevő mennyiségi tárolóhoz tartozó feladatátvételi feladatokat indítja el.</span><span class="sxs-lookup"><span data-stu-id="e6487-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="e6487-124">A parancs az eszköz AZONOSÍTÓját és a céleszköz AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6487-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="e6487-125">A parancs a parancsmag által elindított feladat példányának AZONOSÍTÓját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e6487-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="e6487-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6487-126">PARAMETERS</span></span>

### <span data-ttu-id="e6487-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e6487-127">-DeviceId</span></span>
<span data-ttu-id="e6487-128">Annak az StorSimple-eszköznek a példány-AZONOSÍTÓját adja meg, amelyen a mennyiségi tároló csoport létezik.</span><span class="sxs-lookup"><span data-stu-id="e6487-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6487-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e6487-129">-DeviceName</span></span>
<span data-ttu-id="e6487-130">Annak a StorSimple-eszköznek a nevét adja meg, amelyen a mennyiségi tároló csoport létezik.</span><span class="sxs-lookup"><span data-stu-id="e6487-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6487-131">-Force</span><span class="sxs-lookup"><span data-stu-id="e6487-131">-Force</span></span>
<span data-ttu-id="e6487-132">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e6487-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6487-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="e6487-133">-Profile</span></span>
<span data-ttu-id="e6487-134">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="e6487-134">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6487-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="e6487-135">-TargetDeviceId</span></span>
<span data-ttu-id="e6487-136">Annak az StorSimple-eszköznek a példány-AZONOSÍTÓját adja meg, amelyre a parancsmag a mennyiségi tároló csoporton keresztül nem ér el.</span><span class="sxs-lookup"><span data-stu-id="e6487-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6487-137">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="e6487-137">-TargetDeviceName</span></span>
<span data-ttu-id="e6487-138">Annak a StorSimple-eszköznek a nevét adja meg, amelyre a parancsmag a mennyiségi tároló csoporton keresztül nem képes.</span><span class="sxs-lookup"><span data-stu-id="e6487-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6487-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="e6487-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="e6487-140">Azon mennyiségi tároló-csoportok listáját adja meg, amelyeket a parancsmag a másik eszközre nem ér át.</span><span class="sxs-lookup"><span data-stu-id="e6487-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6487-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6487-141">CommonParameters</span></span>
<span data-ttu-id="e6487-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6487-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6487-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6487-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6487-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6487-144">INPUTS</span></span>

### <span data-ttu-id="e6487-145">Lista\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="e6487-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="e6487-146">A kötet-tároló csoportok listáját áthelyezheti erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="e6487-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="e6487-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6487-147">OUTPUTS</span></span>

### <span data-ttu-id="e6487-148">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="e6487-148">String</span></span>

## <span data-ttu-id="e6487-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6487-149">NOTES</span></span>

## <span data-ttu-id="e6487-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6487-150">RELATED LINKS</span></span>

[<span data-ttu-id="e6487-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="e6487-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


