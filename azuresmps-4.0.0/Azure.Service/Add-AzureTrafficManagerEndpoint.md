---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016376"
---
# <span data-ttu-id="b3f80-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3f80-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b3f80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3f80-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f80-103">Hozzáad egy végpontot a forgalomirányító profiljához.</span><span class="sxs-lookup"><span data-stu-id="b3f80-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="b3f80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3f80-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b3f80-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3f80-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f80-106">A **Add-AzureTrafficManagerEndpoint** parancsmag egy végpontot ad hozzá egy Microsoft Azure Traffic Manager-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="b3f80-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b3f80-107">Miután hozzáadta a végpontot, átadja az eredményt a **set-AzureTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="b3f80-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b3f80-108">Ez a parancsmag az Azure-hoz csatlakozik a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="b3f80-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="b3f80-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b3f80-109">EXAMPLES</span></span>

### <span data-ttu-id="b3f80-110">1. példa: végpont felvétele a profilba</span><span class="sxs-lookup"><span data-stu-id="b3f80-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="b3f80-111">Az első parancs a **Get-AzureTrafficManagerProfile** parancsmagot használja a ContosoProfile nevű profil beolvasásához, majd a $TrafficManagerProfile változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b3f80-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b3f80-112">A második parancs a $TrafficManagerProfile-on tárolt Traffic Manager-profilhoz ad hozzá egy végpontot.</span><span class="sxs-lookup"><span data-stu-id="b3f80-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b3f80-113">A végpont a Contoso02App.couldapp.net tartománynév.</span><span class="sxs-lookup"><span data-stu-id="b3f80-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="b3f80-114">A parancs azt is megadhatja, hogy engedélyezve van-e a típusa.</span><span class="sxs-lookup"><span data-stu-id="b3f80-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="b3f80-115">A parancs átadja a profil objektumnak a **set-AzureTrafficManagerProfile** parancsmagot az Azure-hoz való csatlakozáshoz a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="b3f80-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="b3f80-116">2. példa: meghatározott helyet és vastagságot tartalmazó végpont felvétele</span><span class="sxs-lookup"><span data-stu-id="b3f80-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="b3f80-117">Ez a parancs egy végpontot ad a forgalomirányító-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="b3f80-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="b3f80-118">A végpont a Contoso02App.couldapp.net tartománynév.</span><span class="sxs-lookup"><span data-stu-id="b3f80-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="b3f80-119">A parancs azt is megadhatja, hogy engedélyezve van-e a típusa.</span><span class="sxs-lookup"><span data-stu-id="b3f80-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="b3f80-120">A parancs a végpont vastagságát és helyét is megadja.</span><span class="sxs-lookup"><span data-stu-id="b3f80-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="b3f80-121">A parancs átadja a AzureTrafficManagerProfile az Azure **-** hoz való csatlakozáshoz a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="b3f80-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="b3f80-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3f80-122">PARAMETERS</span></span>

### <span data-ttu-id="b3f80-123">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="b3f80-123">-DomainName</span></span>
<span data-ttu-id="b3f80-124">A hozzáadni kívánt végpont tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3f80-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="b3f80-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="b3f80-125">-Location</span></span>
<span data-ttu-id="b3f80-126">A parancsmag által hozzáadott végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3f80-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="b3f80-127">Ehhez az Azure-helynek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b3f80-127">This must be an Azure location.</span></span>

<span data-ttu-id="b3f80-128">Ennek a paraméternek tartalmaznia kell egy, az "any" vagy a "TrafficManager" típusú végpontok értékét egy olyan profilban, amelyben a "teljesítmény" értékre van állítva a terheléselosztási módszer.</span><span class="sxs-lookup"><span data-stu-id="b3f80-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="b3f80-129">A lehetséges értékek az Azure-körzetek nevei, az itt látható módon https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="b3f80-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="b3f80-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="b3f80-130">-MinChildEndpoints</span></span>
<span data-ttu-id="b3f80-131">A végpontok minimális számának meghatározása: a beágyazott profilnak online kell lennie ahhoz, hogy a végpont online állapotú legyen.</span><span class="sxs-lookup"><span data-stu-id="b3f80-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f80-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="b3f80-132">-Profile</span></span>
<span data-ttu-id="b3f80-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b3f80-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b3f80-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b3f80-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3f80-135">-Állapot</span><span class="sxs-lookup"><span data-stu-id="b3f80-135">-Status</span></span>
<span data-ttu-id="b3f80-136">A figyelési végpont állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3f80-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="b3f80-137">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b3f80-137">Valid values are:</span></span> 

- <span data-ttu-id="b3f80-138">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="b3f80-138">Enabled</span></span>
- <span data-ttu-id="b3f80-139">Tiltva</span><span class="sxs-lookup"><span data-stu-id="b3f80-139">Disabled</span></span>

<span data-ttu-id="b3f80-140">Ha megadja az engedélyezett értéket, a Traffic Manager figyeli a végpontot, és a terheléselosztási módszer a forgalom kezelésekor tartja a betöltést.</span><span class="sxs-lookup"><span data-stu-id="b3f80-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="b3f80-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3f80-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="b3f80-142">Annak a Traffic Manager-profil objektumnak a megadása, amelyhez hozzá szeretné adni a végpontot.</span><span class="sxs-lookup"><span data-stu-id="b3f80-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f80-143">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="b3f80-143">-Type</span></span>
<span data-ttu-id="b3f80-144">A végpont típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3f80-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="b3f80-145">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b3f80-145">Valid values are:</span></span> 

- <span data-ttu-id="b3f80-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="b3f80-146">CloudService</span></span>
- <span data-ttu-id="b3f80-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b3f80-147">AzureWebsite</span></span>
- <span data-ttu-id="b3f80-148">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b3f80-148">TrafficManager</span></span>

- <span data-ttu-id="b3f80-149">Bármely</span><span class="sxs-lookup"><span data-stu-id="b3f80-149">Any</span></span> 

<span data-ttu-id="b3f80-150">Ha egynél több AzureWebsite-végpont van, a végpontoknak különböző adatközpontokban kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="b3f80-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="b3f80-151">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="b3f80-151">-Weight</span></span>
<span data-ttu-id="b3f80-152">A parancsmag által hozzáadott végpont vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3f80-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="b3f80-153">A paraméterhez tartozó érvényes értéktartomány \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="b3f80-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="b3f80-154">Ez a paraméter csak a RoundRobin terheléselosztási házirendek esetében használatos.</span><span class="sxs-lookup"><span data-stu-id="b3f80-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f80-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f80-155">CommonParameters</span></span>
<span data-ttu-id="b3f80-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3f80-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f80-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3f80-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f80-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3f80-158">INPUTS</span></span>

## <span data-ttu-id="b3f80-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3f80-159">OUTPUTS</span></span>

### <span data-ttu-id="b3f80-160">Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="b3f80-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="b3f80-161">Ez a parancsmag a Traffic Manager profil objektumát hozza létre, amely a frissített profillal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b3f80-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="b3f80-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3f80-162">NOTES</span></span>

## <span data-ttu-id="b3f80-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3f80-163">RELATED LINKS</span></span>

[<span data-ttu-id="b3f80-164">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3f80-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="b3f80-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3f80-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="b3f80-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3f80-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b3f80-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3f80-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


