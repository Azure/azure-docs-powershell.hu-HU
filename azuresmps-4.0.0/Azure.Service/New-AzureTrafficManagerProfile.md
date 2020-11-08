---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016202"
---
# <span data-ttu-id="3f770-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f770-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="3f770-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f770-102">SYNOPSIS</span></span>
<span data-ttu-id="3f770-103">Forgalomirányító-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3f770-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="3f770-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f770-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f770-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f770-105">DESCRIPTION</span></span>
<span data-ttu-id="3f770-106">A **New-AzureTrafficManagerProfile** parancsmag létrehoz egy Microsoft Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="3f770-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="3f770-107">Miután létrehozta azt a profilt, amelyben a *LoadBalancingMethod* értékét a "feladatátvétel" értékre állítja, a Add-AzureTrafficManagerEndpoint parancsmaggal meghatározhatja a profiljához hozzáadott végpontok feladatátvételi sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="3f770-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="3f770-108">További információ: 2. példa.</span><span class="sxs-lookup"><span data-stu-id="3f770-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="3f770-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3f770-109">EXAMPLES</span></span>

### <span data-ttu-id="3f770-110">Példa 1: Traffic Manager-profil létrehozása</span><span class="sxs-lookup"><span data-stu-id="3f770-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="3f770-111">Ez a parancs létrehoz egy MyProfile nevű forgalomirányítási profilt a megadott forgalomirányítási tartományban egy ciklikus multiplexelés-terheléselosztási módszerrel, 30 másodperces ÉLETTARTAMmal, HTTP-figyelési protokollal, a 80-es port figyelésével és a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="3f770-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="3f770-112">2. példa: a végpontok átrendezése a kívánt feladatátvételi sorrendbe</span><span class="sxs-lookup"><span data-stu-id="3f770-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="3f770-113">Ebben a példában átrendezi a MyProfile hozzáadott végpontokat a kívánt feladatátvételi sorrendbe.</span><span class="sxs-lookup"><span data-stu-id="3f770-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="3f770-114">Az első parancs beolvassa a Traffic Manager profil objektum MyProfile nevű objektumát, és a $Profile változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="3f770-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="3f770-115">A második parancs átrendezi a végpontokat a végpontok tömbből arra a sorrendre, amelyben a feladatátvételt meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="3f770-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="3f770-116">Az utolsó parancs frissíti a $Profileban tárolt forgalomirányítási profilt az új végponti sorrendben.</span><span class="sxs-lookup"><span data-stu-id="3f770-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="3f770-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f770-117">PARAMETERS</span></span>

### <span data-ttu-id="3f770-118">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="3f770-118">-DomainName</span></span>
<span data-ttu-id="3f770-119">A Traffic Manager-profil tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f770-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="3f770-120">Ennek a trafficmanager.net altartománynak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3f770-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="3f770-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="3f770-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="3f770-122">A kapcsolat elosztásához használt terheléselosztási módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f770-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="3f770-123">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3f770-123">Valid values are:</span></span> 

- <span data-ttu-id="3f770-124">Teljesítmény</span><span class="sxs-lookup"><span data-stu-id="3f770-124">Performance</span></span>
- <span data-ttu-id="3f770-125">Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="3f770-125">Failover</span></span>
- <span data-ttu-id="3f770-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="3f770-126">RoundRobin</span></span>

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

### <span data-ttu-id="3f770-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="3f770-127">-MonitorPort</span></span>
<span data-ttu-id="3f770-128">A végpontok állapotának figyeléséhez használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f770-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="3f770-129">Az érvényes értékek a 0 és kisebb, mint 65 535-nél nagyobb egész számok.</span><span class="sxs-lookup"><span data-stu-id="3f770-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f770-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="3f770-130">-MonitorProtocol</span></span>
<span data-ttu-id="3f770-131">A végpontok állapotának figyeléséhez használható protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f770-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="3f770-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3f770-132">Valid values are:</span></span> 

- <span data-ttu-id="3f770-133">Http</span><span class="sxs-lookup"><span data-stu-id="3f770-133">Http</span></span>

- <span data-ttu-id="3f770-134">Https</span><span class="sxs-lookup"><span data-stu-id="3f770-134">Https</span></span>

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

### <span data-ttu-id="3f770-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="3f770-135">-MonitorRelativePath</span></span>
<span data-ttu-id="3f770-136">A végponthoz viszonyított elérési utat adja meg a szonda állapotához</span><span class="sxs-lookup"><span data-stu-id="3f770-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="3f770-137">Az elérési útnak az alábbi korlátozásoknak kell megfelelnie:</span><span class="sxs-lookup"><span data-stu-id="3f770-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="3f770-138">Az elérési útnak 1-től 1000 karakterből kell állnia.</span><span class="sxs-lookup"><span data-stu-id="3f770-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="3f770-139">Meg kell kezdődnie egy perjelet,/.</span><span class="sxs-lookup"><span data-stu-id="3f770-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="3f770-140">Tartalmaznia kell az XML-elemeket \<\> .</span><span class="sxs-lookup"><span data-stu-id="3f770-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="3f770-141">Nem tartalmazhat dupla ferdeség,//.</span><span class="sxs-lookup"><span data-stu-id="3f770-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="3f770-142">Nem tartalmazhat érvénytelen HTML-Escape-karaktereket.</span><span class="sxs-lookup"><span data-stu-id="3f770-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="3f770-143">Például:% XY.</span><span class="sxs-lookup"><span data-stu-id="3f770-143">For example, %XY.</span></span>

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

### <span data-ttu-id="3f770-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f770-144">-Name</span></span>
<span data-ttu-id="3f770-145">A létrehozandó forgalomirányítási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f770-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f770-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f770-146">-Profile</span></span>
<span data-ttu-id="3f770-147">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3f770-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3f770-148">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3f770-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f770-149">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="3f770-149">-Ttl</span></span>
<span data-ttu-id="3f770-150">Azt a DNS-élettartamot adja meg, amely a helyi DNS-megoldókat a DNS-rekordok gyorsítótárazását követően adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f770-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="3f770-151">Az érvényes értékek a 30 és a 999 999 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="3f770-151">Valid values are integers from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f770-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f770-152">CommonParameters</span></span>
<span data-ttu-id="3f770-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f770-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f770-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f770-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f770-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f770-155">INPUTS</span></span>

## <span data-ttu-id="3f770-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f770-156">OUTPUTS</span></span>

### <span data-ttu-id="3f770-157">Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="3f770-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="3f770-158">Ez a parancsmag a Traffic Manager profil objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="3f770-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="3f770-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f770-159">NOTES</span></span>

## <span data-ttu-id="3f770-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f770-160">RELATED LINKS</span></span>

[<span data-ttu-id="3f770-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f770-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3f770-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f770-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3f770-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f770-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3f770-164">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f770-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3f770-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f770-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


