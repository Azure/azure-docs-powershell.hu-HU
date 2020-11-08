---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015996"
---
# <span data-ttu-id="ed8cb-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ed8cb-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="ed8cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8cb-103">Azure RemoteApp-gyűjteményt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="ed8cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed8cb-104">SYNTAX</span></span>

### <span data-ttu-id="ed8cb-105">AllParameterSets (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed8cb-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ed8cb-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="ed8cb-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed8cb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed8cb-107">DESCRIPTION</span></span>
<span data-ttu-id="ed8cb-108">A **New-AzureRemoteAppCollection** parancsmag létrehoz egy Azure RemoteApp-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="ed8cb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ed8cb-109">EXAMPLES</span></span>

### <span data-ttu-id="ed8cb-110">Példa 1: gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="ed8cb-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="ed8cb-111">A parancs Azure RemoteApp-gyűjteményt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="ed8cb-112">2. példa: gyűjtemény létrehozása hitelesítő adatokkal</span><span class="sxs-lookup"><span data-stu-id="ed8cb-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="ed8cb-113">A parancs a **Get-hitelesítőadat** parancsmag hitelesítő adataival hoz létre Azure RemoteApp-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="ed8cb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed8cb-114">PARAMETERS</span></span>

### <span data-ttu-id="ed8cb-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="ed8cb-115">-CollectionName</span></span>
<span data-ttu-id="ed8cb-116">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-116">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-117">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="ed8cb-117">-Credential</span></span>
<span data-ttu-id="ed8cb-118">Megadja egy olyan szolgáltatásfiók hitelesítő adatait, amely engedéllyel rendelkezik az Azure RemoteApp kiszolgálókhoz való csatlakozáshoz a tartományához.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="ed8cb-119">Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="ed8cb-120">-CustomRdpProperty</span></span>
<span data-ttu-id="ed8cb-121">Az egyéni RDP-tulajdonságokat adja meg, amelyek a meghajtó-átirányítás és az egyéb beállítások konfigurálására használhatók.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="ed8cb-122">További információt az [RDP-beállítások a Windows Server Remote Desktop Services szolgáltatáshoz](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) című témakörben talál `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="ed8cb-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

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

### <span data-ttu-id="ed8cb-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ed8cb-123">-Description</span></span>
<span data-ttu-id="ed8cb-124">Az objektum rövid leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-124">Specifies a short description for the object.</span></span>

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

### <span data-ttu-id="ed8cb-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="ed8cb-125">-DnsServers</span></span>
<span data-ttu-id="ed8cb-126">A DNS-kiszolgálók IPv4-címeinek pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-127">-Tartomány</span><span class="sxs-lookup"><span data-stu-id="ed8cb-127">-Domain</span></span>
<span data-ttu-id="ed8cb-128">Annak az Active Directory tartományi szolgáltatások tartománynak a neve, amelyhez csatlakozni szeretne a távoli asztali munkamenetgazda-kiszolgálókhoz.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-129">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ed8cb-129">-ImageName</span></span>
<span data-ttu-id="ed8cb-130">Az Azure RemoteApp-sablon képének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-130">Specifies the name of the Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="ed8cb-131">-Location</span></span>
<span data-ttu-id="ed8cb-132">A gyűjtemény Azure-régióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-132">Specifies the Azure region of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="ed8cb-133">-OrganizationalUnit</span></span>
<span data-ttu-id="ed8cb-134">Annak a szervezeti egységnek (OU) a nevét adja meg, amelyhez csatlakozni szeretne a TERMINÁLKISZOLGÁLÓhoz, például OU = MyOu, DC = MyDomain, DC = ParentDomain, DC = com.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="ed8cb-135">Az OU-és egyenáramú attribútumoknak nagybetűs kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="ed8cb-136">A program a gyűjtemény létrehozása után nem módosíthatja a szervezeti egységet.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-137">-Terv</span><span class="sxs-lookup"><span data-stu-id="ed8cb-137">-Plan</span></span>
<span data-ttu-id="ed8cb-138">Az Azure RemoteApp-gyűjtemény csomagját adja meg, amely meghatározhatja a használati korlátozásokat.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="ed8cb-139">Az elérhető csomagok megtekintéséhez használja a **Get-AzureRemoteAppPlan** .</span><span class="sxs-lookup"><span data-stu-id="ed8cb-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

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

### <span data-ttu-id="ed8cb-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="ed8cb-140">-Profile</span></span>
<span data-ttu-id="ed8cb-141">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed8cb-142">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed8cb-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ed8cb-143">-ResourceType</span></span>
<span data-ttu-id="ed8cb-144">A gyűjtemény erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="ed8cb-145">A paraméter elfogadható értékei a következők: app vagy asztali.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ed8cb-146">-SubnetName</span></span>
<span data-ttu-id="ed8cb-147">Megadja annak a virtuális hálózatnak a nevét, amellyel az Azure RemoteApp gyűjteményt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ed8cb-148">-VNetName</span></span>
<span data-ttu-id="ed8cb-149">Egy Azure RemoteApp virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed8cb-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8cb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8cb-150">CommonParameters</span></span>
<span data-ttu-id="ed8cb-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed8cb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8cb-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8cb-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8cb-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed8cb-153">INPUTS</span></span>

## <span data-ttu-id="ed8cb-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed8cb-154">OUTPUTS</span></span>

## <span data-ttu-id="ed8cb-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed8cb-155">NOTES</span></span>

## <span data-ttu-id="ed8cb-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed8cb-156">RELATED LINKS</span></span>

[<span data-ttu-id="ed8cb-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ed8cb-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="ed8cb-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="ed8cb-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="ed8cb-159">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ed8cb-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="ed8cb-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ed8cb-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="ed8cb-161">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ed8cb-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


