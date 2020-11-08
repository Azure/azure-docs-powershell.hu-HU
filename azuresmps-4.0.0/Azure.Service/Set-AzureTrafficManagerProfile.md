---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015794"
---
# <span data-ttu-id="d3ba4-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d3ba4-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="d3ba4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ba4-103">Frissíti a forgalomirányító-profilok tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="d3ba4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3ba4-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3ba4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ba4-106">A **set-AzureTrafficManagerProfile** parancsmag frissíti a Microsoft Azure Traffic Manager-profilok tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="d3ba4-107">Azoknál a profiloknál, amelyeknél a *LoadBalancingMethod* értékét a "feladatátvétel" értékre állította, a Add-AzureTrafficManagerEndpoint parancsmaggal meghatározhatja a profiljához hozzáadott végpontok feladatátvételi sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="d3ba4-108">További információért lásd alább a 3.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="d3ba4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d3ba4-109">EXAMPLES</span></span>

### <span data-ttu-id="d3ba4-110">Példa 1: a forgalomirányító-profil TTL-beállítása</span><span class="sxs-lookup"><span data-stu-id="d3ba4-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="d3ba4-111">Ez a parancs a forgalmi vezető profil objektum MyTrafficManagerProfile a TTL (élettartam) értéket 60 másodpercre állítja.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="d3ba4-112">2. példa: több érték beállítása egy profilhoz</span><span class="sxs-lookup"><span data-stu-id="d3ba4-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="d3ba4-113">Ez a parancs a **Get-AzureTrafficManagerProfile** parancsmaggal kapja meg a MyProfile nevű Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="d3ba4-114">A profil a RoundRobin-terheléselosztási módszert, a 30 másodperces ÉLETTARTAMot, a monitor Protocol HTTP-t, a monitor portot és a forgalomirányító-profil relatív elérési útját használja.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="d3ba4-115">3. példa: a végpontok átrendezése a kívánt feladatátvételi sorrendbe</span><span class="sxs-lookup"><span data-stu-id="d3ba4-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="d3ba4-116">Ebben a példában átrendezi a MyProfile hozzáadott végpontokat a kívánt feladatátvételi sorrendbe.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="d3ba4-117">Az első parancs beolvassa a Traffic Manager profil objektum MyProfile nevű objektumát, és a $Profile változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="d3ba4-118">A második parancs átrendezi a végpontokat a végpontok tömbből arra a sorrendre, amelyben a feladatátvételt meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="d3ba4-119">Az utolsó parancs frissíti a $Profileban tárolt forgalomirányítási profilt az új végponti sorrendben.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="d3ba4-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3ba4-120">PARAMETERS</span></span>

### <span data-ttu-id="d3ba4-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="d3ba4-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="d3ba4-122">A kapcsolat elosztásához használt terheléselosztási módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="d3ba4-123">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-123">Valid values are:</span></span> 

- <span data-ttu-id="d3ba4-124">Teljesítmény</span><span class="sxs-lookup"><span data-stu-id="d3ba4-124">Performance</span></span>
- <span data-ttu-id="d3ba4-125">Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="d3ba4-125">Failover</span></span>
- <span data-ttu-id="d3ba4-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="d3ba4-126">RoundRobin</span></span>

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

### <span data-ttu-id="d3ba4-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="d3ba4-127">-MonitorPort</span></span>
<span data-ttu-id="d3ba4-128">A végpontok állapotának figyeléséhez használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="d3ba4-129">Az érvényes értékek a 0 és kisebb, mint 65 535-nél nagyobb egész számok.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="d3ba4-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="d3ba4-130">-MonitorProtocol</span></span>
<span data-ttu-id="d3ba4-131">A végpontok állapotának figyeléséhez használható protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="d3ba4-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-132">Valid values are:</span></span> 

- <span data-ttu-id="d3ba4-133">Http</span><span class="sxs-lookup"><span data-stu-id="d3ba4-133">Http</span></span>
- <span data-ttu-id="d3ba4-134">Https</span><span class="sxs-lookup"><span data-stu-id="d3ba4-134">Https</span></span>

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

### <span data-ttu-id="d3ba4-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="d3ba4-135">-MonitorRelativePath</span></span>
<span data-ttu-id="d3ba4-136">A végponthoz viszonyított elérési utat adja meg a szonda állapotához</span><span class="sxs-lookup"><span data-stu-id="d3ba4-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="d3ba4-137">Az elérési útnak az alábbi korlátozásoknak kell megfelelnie:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="d3ba4-138">Az elérési útnak 1-től 1000 karakterből kell állnia.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="d3ba4-139">Meg kell kezdődnie egy perjelet,/.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="d3ba4-140">Tartalmaznia kell az XML-elemeket \<\> .</span><span class="sxs-lookup"><span data-stu-id="d3ba4-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="d3ba4-141">Nem tartalmazhat dupla ferdeség,//.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="d3ba4-142">Nem tartalmazhat érvénytelen HTML-Escape-karaktereket.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="d3ba4-143">Például:% XY.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-143">For example, %XY.</span></span>

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

### <span data-ttu-id="d3ba4-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3ba4-144">-Name</span></span>
<span data-ttu-id="d3ba4-145">A frissítendő forgalomirányítási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ba4-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="d3ba4-146">-Profile</span></span>
<span data-ttu-id="d3ba4-147">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d3ba4-148">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3ba4-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d3ba4-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="d3ba4-150">A Traffic Manager profil objektumát adja meg a profil beállításához.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

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

### <span data-ttu-id="d3ba4-151">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="d3ba4-151">-Ttl</span></span>
<span data-ttu-id="d3ba4-152">Azt a DNS-élettartamot adja meg, amely a helyi DNS-megoldókat a DNS-rekordok gyorsítótárazását követően adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="d3ba4-153">Az érvényes értékek a 30 és a 999 999 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-153">Valid values are an integer from 30 through 999,999.</span></span>

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

### <span data-ttu-id="d3ba4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ba4-154">CommonParameters</span></span>
<span data-ttu-id="d3ba4-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3ba4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ba4-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ba4-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ba4-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3ba4-157">INPUTS</span></span>

## <span data-ttu-id="d3ba4-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3ba4-158">OUTPUTS</span></span>

### <span data-ttu-id="d3ba4-159">Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="d3ba4-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="d3ba4-160">Ez a parancsmag a Traffic Manager profil objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="d3ba4-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3ba4-161">NOTES</span></span>

## <span data-ttu-id="d3ba4-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3ba4-162">RELATED LINKS</span></span>

[<span data-ttu-id="d3ba4-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d3ba4-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d3ba4-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d3ba4-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d3ba4-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d3ba4-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d3ba4-166">Új – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d3ba4-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d3ba4-167">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d3ba4-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


