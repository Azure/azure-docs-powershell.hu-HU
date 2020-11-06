---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 0568359131a91beeb175d69da51d1646bd28f88e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492377"
---
# <span data-ttu-id="02512-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="02512-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="02512-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02512-102">SYNOPSIS</span></span>
<span data-ttu-id="02512-103">Helyi konfigurációs objektum létrehozása tároló szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="02512-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02512-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02512-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02512-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02512-105">DESCRIPTION</span></span>
<span data-ttu-id="02512-106">A **New-AzureRmContainerServiceConfig** parancsmag létrehoz egy helyi konfigurációs objektumot egy tároló szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="02512-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="02512-107">Ezt az objektumot a New-AzureRmContainerService parancsmaggal hozhatja létre tároló szolgáltatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="02512-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="02512-108">Példák</span><span class="sxs-lookup"><span data-stu-id="02512-108">EXAMPLES</span></span>

### <span data-ttu-id="02512-109">Példa 1: tároló szolgáltatás konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="02512-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="02512-110">Ez a parancs létrehoz egy tárolót, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02512-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="02512-111">A parancs a tároló szolgáltatás konfigurációjának különféle beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="02512-112">A parancs átadja a konfigurációs objektumot a Add-AzureRmContainerServiceAgentPoolProfile parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="02512-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="02512-113">Ez a parancsmag egy Agent Pool-profilt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="02512-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="02512-114">Adja meg az objektumot $Container a **New-AzureRmContainerService** *ContainerService* paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="02512-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="02512-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02512-115">PARAMETERS</span></span>

### <span data-ttu-id="02512-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="02512-116">-AdminUsername</span></span>
<span data-ttu-id="02512-117">A Linux-alapú tároló szolgáltatáshoz használt rendszergazdai fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="02512-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="02512-118">-AgentPoolProfile</span></span>
<span data-ttu-id="02512-119">A tároló szolgáltatáshoz tartozó Agent Pool-profil objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="02512-120">Profil hozzáadása a Add-AzureRmContainerServiceAgentPoolProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="02512-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="02512-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="02512-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="02512-122">Az egyéni profil Orchestrator adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="02512-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="02512-123">-Location</span></span>
<span data-ttu-id="02512-124">A tároló szolgáltatás létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-124">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="02512-125">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="02512-125">-MasterCount</span></span>
<span data-ttu-id="02512-126">A létrehozandó fő virtuális gépek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-126">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="02512-127">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="02512-127">-MasterDnsPrefix</span></span>
<span data-ttu-id="02512-128">A fő virtuális gép DNS-előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-128">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="02512-129">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="02512-129">-OrchestratorType</span></span>
<span data-ttu-id="02512-130">A tároló szolgáltatás Orchestrator típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-130">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="02512-131">A paraméter elfogadható értékei a következők: DCOS és raj.</span><span class="sxs-lookup"><span data-stu-id="02512-131">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="02512-132">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="02512-132">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="02512-133">A fő profil ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-133">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="02512-134">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="02512-134">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="02512-135">A fő profil titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-135">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="02512-136">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="02512-136">-SshPublicKey</span></span>
<span data-ttu-id="02512-137">A Linux-alapú tároló szolgáltatás SSH-beli nyilvános kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-137">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="02512-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="02512-138">-Tag</span></span>
<span data-ttu-id="02512-139">A tároló szolgáltatás címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-139">Specifies tags for the container service.</span></span>

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

### <span data-ttu-id="02512-140">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="02512-140">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="02512-141">Azt jelzi, hogy ez a konfiguráció engedélyezi-e a diagnosztikát a tároló szolgáltatás virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="02512-141">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="02512-142">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="02512-142">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="02512-143">Megadja a Windows operációs rendszert használó tároló-szolgáltatás rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="02512-143">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="02512-144">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="02512-144">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="02512-145">A Windows operációs rendszert használó tároló szolgáltatás rendszergazdai felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02512-145">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="02512-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02512-146">-Confirm</span></span>
<span data-ttu-id="02512-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02512-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02512-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02512-148">-WhatIf</span></span>
<span data-ttu-id="02512-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02512-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02512-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02512-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02512-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02512-151">CommonParameters</span></span>
<span data-ttu-id="02512-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02512-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02512-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02512-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02512-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02512-154">INPUTS</span></span>

### <span data-ttu-id="02512-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="02512-155">None</span></span>
<span data-ttu-id="02512-156">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="02512-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02512-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02512-157">OUTPUTS</span></span>

## <span data-ttu-id="02512-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02512-158">NOTES</span></span>

## <span data-ttu-id="02512-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02512-159">RELATED LINKS</span></span>

[<span data-ttu-id="02512-160">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="02512-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="02512-161">Új – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="02512-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


