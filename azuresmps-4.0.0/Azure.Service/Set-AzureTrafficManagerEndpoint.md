---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015434"
---
# <span data-ttu-id="6df19-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6df19-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="6df19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6df19-102">SYNOPSIS</span></span>
<span data-ttu-id="6df19-103">Frissíti egy végpont tulajdonságait a forgalomirányítási profilban.</span><span class="sxs-lookup"><span data-stu-id="6df19-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="6df19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6df19-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6df19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6df19-105">DESCRIPTION</span></span>
<span data-ttu-id="6df19-106">A **set-AzureTrafficManagerEndpoint** parancsmag frissíti egy végpont tulajdonságait egy Microsoft Azure Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="6df19-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="6df19-107">Ha a végpont nem létezik az aktuális profilban, ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6df19-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="6df19-108">Miután hozzáadta a végpontot, átadja az eredményt a **set-AzureTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="6df19-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6df19-109">Ez a parancsmag az Azure-hoz csatlakozik a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="6df19-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="6df19-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6df19-110">EXAMPLES</span></span>

### <span data-ttu-id="6df19-111">1. példa: a végpontok frissítése egy profilhoz</span><span class="sxs-lookup"><span data-stu-id="6df19-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="6df19-112">Az első parancs a **Get-AzureTrafficManagerProfile** parancsmagot használja a ContosoProfile nevű profil beolvasásához, majd a $TrafficManagerProfile változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6df19-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="6df19-113">A második parancs a $TrafficManagerProfile-on tárolt forgalomirányítási profilban frissíti a végpontot.</span><span class="sxs-lookup"><span data-stu-id="6df19-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="6df19-114">A végpont a ContosoApp02.cloudapp.net tartománynév.</span><span class="sxs-lookup"><span data-stu-id="6df19-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="6df19-115">A parancs a végpont állapotát, típusát, vastagságát és helyét is megadja.</span><span class="sxs-lookup"><span data-stu-id="6df19-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="6df19-116">A parancs a módosított profilt átadja a **set-AzureTrafficManagerProfile** parancsmagnak, amellyel az Azure-hoz kapcsolódhat a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="6df19-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="6df19-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6df19-117">PARAMETERS</span></span>

### <span data-ttu-id="6df19-118">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="6df19-118">-DomainName</span></span>
<span data-ttu-id="6df19-119">A módosítandó végpont tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6df19-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="6df19-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="6df19-120">-Location</span></span>
<span data-ttu-id="6df19-121">A parancsmag által hozzáadott végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6df19-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="6df19-122">Ehhez az Azure-helynek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6df19-122">This must be an Azure location.</span></span>

<span data-ttu-id="6df19-123">Ennek a paraméternek tartalmaznia kell egy, az "any" vagy a "TrafficManager" típusú végpontok értékét egy olyan profilban, amelyben a "teljesítmény" értékre van állítva a terheléselosztási módszer.</span><span class="sxs-lookup"><span data-stu-id="6df19-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="6df19-124">A lehetséges értékek az Azure-körzetek nevei, az itt látható módon  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="6df19-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="6df19-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="6df19-125">-MinChildEndpoints</span></span>
<span data-ttu-id="6df19-126">A végpontok minimális számának meghatározása: a beágyazott profilnak online kell lennie ahhoz, hogy a végpont online állapotú legyen.</span><span class="sxs-lookup"><span data-stu-id="6df19-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="6df19-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="6df19-127">-Profile</span></span>
<span data-ttu-id="6df19-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6df19-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6df19-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6df19-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6df19-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="6df19-130">-Status</span></span>
<span data-ttu-id="6df19-131">A figyelési végpont állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6df19-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="6df19-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6df19-132">Valid values are:</span></span> 

- <span data-ttu-id="6df19-133">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="6df19-133">Enabled</span></span>
- <span data-ttu-id="6df19-134">Tiltva</span><span class="sxs-lookup"><span data-stu-id="6df19-134">Disabled</span></span>

<span data-ttu-id="6df19-135">Ha megadja az engedélyezett értéket, a Traffic Manager figyeli a végpontot, és a terheléselosztási módszer a forgalom kezelésekor tartja a betöltést.</span><span class="sxs-lookup"><span data-stu-id="6df19-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="6df19-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6df19-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="6df19-137">Annak a Traffic Manager-profil objektumnak a beállítása, amelynek a végpontját módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="6df19-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="6df19-138">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="6df19-138">-Type</span></span>
<span data-ttu-id="6df19-139">A végpont típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6df19-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="6df19-140">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6df19-140">Valid values are:</span></span> 

- <span data-ttu-id="6df19-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="6df19-141">CloudService</span></span>
- <span data-ttu-id="6df19-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6df19-142">AzureWebsite</span></span>
- <span data-ttu-id="6df19-143">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6df19-143">TrafficManager</span></span>

- <span data-ttu-id="6df19-144">Bármely</span><span class="sxs-lookup"><span data-stu-id="6df19-144">Any</span></span> 

<span data-ttu-id="6df19-145">Ha egynél több AzureWebsite-végpont van, a végpontoknak különböző adatközpontokban kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="6df19-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="6df19-146">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="6df19-146">-Weight</span></span>
<span data-ttu-id="6df19-147">A parancsmag által hozzáadott végpont vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6df19-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="6df19-148">A paraméterhez tartozó érvényes értéktartomány \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="6df19-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="6df19-149">Ez a paraméter csak a RoundRobin terheléselosztási házirendek esetében használatos.</span><span class="sxs-lookup"><span data-stu-id="6df19-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="6df19-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df19-150">CommonParameters</span></span>
<span data-ttu-id="6df19-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6df19-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df19-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df19-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df19-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6df19-153">INPUTS</span></span>

## <span data-ttu-id="6df19-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6df19-154">OUTPUTS</span></span>

### <span data-ttu-id="6df19-155">Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="6df19-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="6df19-156">Ez a parancsmag a Traffic Manager profil objektumát hozza létre, amely a frissített profillal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6df19-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="6df19-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6df19-157">NOTES</span></span>

## <span data-ttu-id="6df19-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6df19-158">RELATED LINKS</span></span>

[<span data-ttu-id="6df19-159">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6df19-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="6df19-160">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6df19-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="6df19-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6df19-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="6df19-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6df19-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


