---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015515"
---
# <span data-ttu-id="85e05-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="85e05-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="85e05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85e05-102">SYNOPSIS</span></span>
<span data-ttu-id="85e05-103">Hálózati konfigurációs objektum előkészítése</span><span class="sxs-lookup"><span data-stu-id="85e05-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="85e05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85e05-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="85e05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85e05-105">DESCRIPTION</span></span>
<span data-ttu-id="85e05-106">A **New-AzureStorSimpleNetworkConfig** parancsmag hálózati konfigurációs objektumra készíti át a **set-AzureStorSimpleDevice** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="85e05-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="85e05-107">Állítsa a *Controller0IPAddress* paramétert és a *Controller1IPAddress* paramétert csak a Data0 felületen.</span><span class="sxs-lookup"><span data-stu-id="85e05-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="85e05-108">A Data0 csak három beállítást támogat: *Controller0IPAddress* , *Controller1IPAdress* és *EnableIscsi*.</span><span class="sxs-lookup"><span data-stu-id="85e05-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="85e05-109">Példák</span><span class="sxs-lookup"><span data-stu-id="85e05-109">EXAMPLES</span></span>

### <span data-ttu-id="85e05-110">1. példa: Data0-felület beállítása</span><span class="sxs-lookup"><span data-stu-id="85e05-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="85e05-111">Ez a parancs hálózati konfigurációt hoz létre a Data0 felületéhez.</span><span class="sxs-lookup"><span data-stu-id="85e05-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="85e05-112">Ez a parancs a *Controller0IPv4Address* , az *Controller1IPv4Address* és a *EnableIscsi* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="85e05-113">Ez a parancsmag csak a következő három paraméterhez tudja konfigurálni a Data0.</span><span class="sxs-lookup"><span data-stu-id="85e05-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="85e05-114">2. példa: Configuren az Data0 eltérő felületet</span><span class="sxs-lookup"><span data-stu-id="85e05-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="85e05-115">Ez a parancs a Data1-felületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="85e05-116">3. példa: eszköz konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="85e05-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="85e05-117">Az első parancs létrehozza az Data0 felület hálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="85e05-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="85e05-118">Ez a parancs a *Controller0IPv4Address* , az *Controller1IPv4Address* és a *EnableIscsi* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="85e05-119">A parancs az eredményt az $NetworkConfigData 0 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="85e05-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="85e05-120">A második parancs a **Get-AzureStorSimpleDevice** parancsmagot és a **Where-Object** Core parancsmagot használja online StorSimple-eszköz beszerzéséhez, majd a $OnlineDevice változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="85e05-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="85e05-121">A végleges parancs a **set-AzureStorSimpleDevice** parancsmaggal módosítja a megadott eszköz-azonosítót tartalmazó eszköz konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="85e05-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="85e05-122">A parancs az első parancsban létrehozott Configuration objektummal használja az aktuális parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="85e05-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="85e05-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85e05-123">PARAMETERS</span></span>

### <span data-ttu-id="85e05-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="85e05-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="85e05-125">A 0 vezérlő IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="85e05-126">Ezt a paramétert csak a Data0 felületéhez adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-126">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="85e05-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="85e05-128">Az 1-es vezérlő IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="85e05-129">Ezt a paramétert csak a Data0 felületéhez adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-129">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="85e05-130">-EnableCloud</span></span>
<span data-ttu-id="85e05-131">Azt jelzi, hogy engedélyezve van-e a felhőalapú beállítás.</span><span class="sxs-lookup"><span data-stu-id="85e05-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="85e05-132">-EnableIscsi</span></span>
<span data-ttu-id="85e05-133">Azt jelzi, hogy engedélyezve van-e az internetes SCSI (ISCSI) az illesztőfelületen.</span><span class="sxs-lookup"><span data-stu-id="85e05-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-134">-InterfaceAlias</span><span class="sxs-lookup"><span data-stu-id="85e05-134">-InterfaceAlias</span></span>
<span data-ttu-id="85e05-135">Annak a kapcsolatnak az illesztőfelület-aliasát adja meg, amelyhez ez a parancsmag a beállításokat szolgáltatja.</span><span class="sxs-lookup"><span data-stu-id="85e05-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="85e05-136">Az érvényes értékek a Data0-től a Data5-ig kerülnek.</span><span class="sxs-lookup"><span data-stu-id="85e05-136">Valid values are from Data0 to Data5.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="85e05-137">-IPv4Address</span></span>
<span data-ttu-id="85e05-138">Az összeköttetés IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-138">Specifies the IPv4 address for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="85e05-139">-IPv4Gateway</span></span>
<span data-ttu-id="85e05-140">Az átjáró IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-140">Specifies the IPv4 address of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="85e05-141">-IPv4Netmask</span></span>
<span data-ttu-id="85e05-142">Az összeköttetéshez tartozó IPv4-hálózati maszkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-142">Specifies the IPv4 netmask for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="85e05-143">-IPv6Gateway</span></span>
<span data-ttu-id="85e05-144">Az összeköttetés IPv6-átjáróját adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-144">Specifies the IPv6 gateway for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="85e05-145">-IPv6Prefix</span></span>
<span data-ttu-id="85e05-146">A felület IPv6-előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-146">Specifies the IPv6 prefix for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="85e05-147">-Profile</span></span>
<span data-ttu-id="85e05-148">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="85e05-148">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="85e05-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e05-149">CommonParameters</span></span>
<span data-ttu-id="85e05-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85e05-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e05-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e05-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e05-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85e05-152">INPUTS</span></span>

### <span data-ttu-id="85e05-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="85e05-153">None</span></span>

## <span data-ttu-id="85e05-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85e05-154">OUTPUTS</span></span>

### <span data-ttu-id="85e05-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="85e05-155">NetworkConfig</span></span>
<span data-ttu-id="85e05-156">Ez a parancsmag egy NetworkConfig objektumot ad eredményül, amely a következő tulajdonságokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="85e05-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="85e05-157">**IsIscsiEnabled** ( **logikai** )</span><span class="sxs-lookup"><span data-stu-id="85e05-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="85e05-158">**IsCloudEnabled** ( **logikai** )</span><span class="sxs-lookup"><span data-stu-id="85e05-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="85e05-159">**Controller0IPv4Address** ( **IP_cím** )</span><span class="sxs-lookup"><span data-stu-id="85e05-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="85e05-160">**Controller1IPv4Address** ( **IP_cím** )</span><span class="sxs-lookup"><span data-stu-id="85e05-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="85e05-161">**IPv6Gateway** ( **IP_cím** )</span><span class="sxs-lookup"><span data-stu-id="85e05-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="85e05-162">**IPv4Gateway** ( **IP_cím** )</span><span class="sxs-lookup"><span data-stu-id="85e05-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="85e05-163">**IPv4Address** ( **IP_cím** )</span><span class="sxs-lookup"><span data-stu-id="85e05-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="85e05-164">**IPv6Prefix** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="85e05-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="85e05-165">**IPv4Netmask** ( **IP_cím** )</span><span class="sxs-lookup"><span data-stu-id="85e05-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="85e05-166">**InterfaceAlias** ( **NetInterfaceId** )</span><span class="sxs-lookup"><span data-stu-id="85e05-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="85e05-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85e05-167">NOTES</span></span>

## <span data-ttu-id="85e05-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85e05-168">RELATED LINKS</span></span>

[<span data-ttu-id="85e05-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="85e05-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="85e05-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="85e05-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


