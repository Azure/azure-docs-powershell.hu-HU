---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: 5631ab93c4c9d0fd89b56043d32bc685b042ace9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667389"
---
# <span data-ttu-id="03ec3-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="03ec3-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="03ec3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="03ec3-103">Helyi konfigurációs objektum létrehozása tároló szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="03ec3-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="03ec3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03ec3-104">SYNTAX</span></span>

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

## <span data-ttu-id="03ec3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="03ec3-106">A **New-AzContainerServiceConfig** parancsmag létrehoz egy helyi konfigurációs objektumot egy tároló szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="03ec3-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="03ec3-107">Ezt az objektumot a New-AzContainerService parancsmaggal hozhatja létre tároló szolgáltatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="03ec3-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="03ec3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="03ec3-108">EXAMPLES</span></span>

### <span data-ttu-id="03ec3-109">Példa 1: tároló szolgáltatás konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="03ec3-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="03ec3-110">Ez a parancs létrehoz egy tárolót, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="03ec3-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="03ec3-111">A parancs a tároló szolgáltatás konfigurációjának különféle beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="03ec3-112">A parancs átadja a konfigurációs objektumot a Add-AzContainerServiceAgentPoolProfile parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="03ec3-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="03ec3-113">Ez a parancsmag egy Agent Pool-profilt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="03ec3-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="03ec3-114">Adja meg az objektumot $Container a **New-AzContainerService** *ContainerService* paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="03ec3-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="03ec3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03ec3-115">PARAMETERS</span></span>

### <span data-ttu-id="03ec3-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="03ec3-116">-AdminUsername</span></span>
<span data-ttu-id="03ec3-117">A Linux-alapú tároló szolgáltatáshoz használt rendszergazdai fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="03ec3-118">-AgentPoolProfile</span></span>
<span data-ttu-id="03ec3-119">A tároló szolgáltatáshoz tartozó Agent Pool-profil objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="03ec3-120">Profil hozzáadása a Add-AzContainerServiceAgentPoolProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="03ec3-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="03ec3-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="03ec3-122">Az egyéni profil Orchestrator adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ec3-123">-DefaultProfile</span></span>
<span data-ttu-id="03ec3-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03ec3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="03ec3-125">-Location</span></span>
<span data-ttu-id="03ec3-126">A tároló szolgáltatás létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="03ec3-127">-MasterCount</span></span>
<span data-ttu-id="03ec3-128">A létrehozandó fő virtuális gépek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="03ec3-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="03ec3-130">A fő virtuális gép DNS-előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="03ec3-131">-OrchestratorType</span></span>
<span data-ttu-id="03ec3-132">A tároló szolgáltatás Orchestrator típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="03ec3-133">A paraméter elfogadható értékei a következők: DCOS és raj.</span><span class="sxs-lookup"><span data-stu-id="03ec3-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="03ec3-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="03ec3-135">A fő profil ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="03ec3-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="03ec3-137">A fő profil titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="03ec3-138">-SshPublicKey</span></span>
<span data-ttu-id="03ec3-139">A Linux-alapú tároló szolgáltatás SSH-beli nyilvános kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="03ec3-140">-Tag</span></span>
<span data-ttu-id="03ec3-141">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="03ec3-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="03ec3-142">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="03ec3-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="03ec3-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="03ec3-144">Azt jelzi, hogy ez a konfiguráció engedélyezi-e a diagnosztikát a tároló szolgáltatás virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="03ec3-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="03ec3-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="03ec3-146">Megadja a Windows operációs rendszert használó tároló-szolgáltatás rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="03ec3-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="03ec3-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="03ec3-148">A Windows operációs rendszert használó tároló szolgáltatás rendszergazdai felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03ec3-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03ec3-149">-Confirm</span></span>
<span data-ttu-id="03ec3-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03ec3-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ec3-151">-WhatIf</span></span>
<span data-ttu-id="03ec3-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03ec3-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03ec3-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03ec3-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ec3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ec3-154">CommonParameters</span></span>
<span data-ttu-id="03ec3-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03ec3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ec3-156">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="03ec3-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ec3-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03ec3-157">INPUTS</span></span>

### <span data-ttu-id="03ec3-158">System. String</span><span class="sxs-lookup"><span data-stu-id="03ec3-158">System.String</span></span>

### <span data-ttu-id="03ec3-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="03ec3-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="03ec3-160">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="03ec3-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="03ec3-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="03ec3-161">System.Int32</span></span>

### <span data-ttu-id="03ec3-162">Microsoft. Azure. Management. számítás. models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="03ec3-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="03ec3-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="03ec3-163">System.String[]</span></span>

### <span data-ttu-id="03ec3-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03ec3-164">System.Boolean</span></span>

## <span data-ttu-id="03ec3-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03ec3-165">OUTPUTS</span></span>

### <span data-ttu-id="03ec3-166">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="03ec3-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="03ec3-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03ec3-167">NOTES</span></span>

## <span data-ttu-id="03ec3-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03ec3-168">RELATED LINKS</span></span>

[<span data-ttu-id="03ec3-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="03ec3-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="03ec3-170">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="03ec3-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
