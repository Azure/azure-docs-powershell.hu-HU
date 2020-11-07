---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: 4352edac7342bd421fb907295581aaa6bee8e8ef
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844502"
---
# <span data-ttu-id="df565-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="df565-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="df565-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df565-102">SYNOPSIS</span></span>
<span data-ttu-id="df565-103">Helyi konfigurációs objektum létrehozása tároló szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="df565-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="df565-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df565-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df565-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df565-105">DESCRIPTION</span></span>
<span data-ttu-id="df565-106">A **New-AzContainerServiceConfig** parancsmag létrehoz egy helyi konfigurációs objektumot egy tároló szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="df565-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="df565-107">Ezt az objektumot a New-AzContainerService parancsmaggal hozhatja létre tároló szolgáltatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="df565-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="df565-108">Példák</span><span class="sxs-lookup"><span data-stu-id="df565-108">EXAMPLES</span></span>

### <span data-ttu-id="df565-109">Példa 1: tároló szolgáltatás konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="df565-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="df565-110">Ez a parancs létrehoz egy tárolót, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="df565-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="df565-111">A parancs a tároló szolgáltatás konfigurációjának különféle beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="df565-112">A parancs átadja a konfigurációs objektumot a Add-AzContainerServiceAgentPoolProfile parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="df565-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="df565-113">Ez a parancsmag egy Agent Pool-profilt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="df565-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="df565-114">Adja meg az objektumot $Container a **New-AzContainerService** *ContainerService* paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="df565-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="df565-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df565-115">PARAMETERS</span></span>

### <span data-ttu-id="df565-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="df565-116">-AdminUsername</span></span>
<span data-ttu-id="df565-117">A Linux-alapú tároló szolgáltatáshoz használt rendszergazdai fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="df565-118">-AgentPoolProfile</span></span>
<span data-ttu-id="df565-119">A tároló szolgáltatáshoz tartozó Agent Pool-profil objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="df565-120">Profil hozzáadása a Add-AzContainerServiceAgentPoolProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="df565-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="df565-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="df565-122">Az egyéni profil Orchestrator adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="df565-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df565-123">-DefaultProfile</span></span>
<span data-ttu-id="df565-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df565-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df565-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="df565-125">-Location</span></span>
<span data-ttu-id="df565-126">A tároló szolgáltatás létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="df565-127">-MasterCount</span></span>
<span data-ttu-id="df565-128">A létrehozandó fő virtuális gépek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="df565-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="df565-130">A fő virtuális gép DNS-előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="df565-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="df565-131">-OrchestratorType</span></span>
<span data-ttu-id="df565-132">A tároló szolgáltatás Orchestrator típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="df565-133">A paraméter elfogadható értékei a következők: DCOS és raj.</span><span class="sxs-lookup"><span data-stu-id="df565-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: ContainerServiceOrchestratorTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="df565-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="df565-135">A fő profil ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="df565-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="df565-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="df565-137">A fő profil titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="df565-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="df565-138">-SshPublicKey</span></span>
<span data-ttu-id="df565-139">A Linux-alapú tároló szolgáltatás SSH-beli nyilvános kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="df565-140">-Tag</span></span>
<span data-ttu-id="df565-141">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="df565-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="df565-142">Példa:</span><span class="sxs-lookup"><span data-stu-id="df565-142">For example:</span></span>

<span data-ttu-id="df565-143">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="df565-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-144">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="df565-144">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="df565-145">Azt jelzi, hogy ez a konfiguráció engedélyezi-e a diagnosztikát a tároló szolgáltatás virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="df565-145">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-146">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="df565-146">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="df565-147">Megadja a Windows operációs rendszert használó tároló-szolgáltatás rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="df565-147">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-148">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="df565-148">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="df565-149">A Windows operációs rendszert használó tároló szolgáltatás rendszergazdai felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df565-149">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df565-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df565-150">-Confirm</span></span>
<span data-ttu-id="df565-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df565-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df565-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df565-152">-WhatIf</span></span>
<span data-ttu-id="df565-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df565-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df565-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df565-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df565-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df565-155">CommonParameters</span></span>
<span data-ttu-id="df565-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df565-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df565-157">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df565-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df565-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df565-158">INPUTS</span></span>

### <span data-ttu-id="df565-159">Nincs</span><span class="sxs-lookup"><span data-stu-id="df565-159">None</span></span>
<span data-ttu-id="df565-160">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="df565-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df565-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df565-161">OUTPUTS</span></span>

### <span data-ttu-id="df565-162">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="df565-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="df565-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df565-163">NOTES</span></span>

## <span data-ttu-id="df565-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df565-164">RELATED LINKS</span></span>

[<span data-ttu-id="df565-165">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="df565-165">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="df565-166">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="df565-166">New-AzContainerService</span></span>](./New-AzContainerService.md)
