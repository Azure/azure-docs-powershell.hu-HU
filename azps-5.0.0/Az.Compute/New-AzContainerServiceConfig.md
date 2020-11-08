---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186790"
---
# <span data-ttu-id="07403-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="07403-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="07403-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07403-102">SYNOPSIS</span></span>
<span data-ttu-id="07403-103">Helyi konfigurációs objektum létrehozása tároló szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="07403-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="07403-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07403-104">SYNTAX</span></span>

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

## <span data-ttu-id="07403-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="07403-105">DESCRIPTION</span></span>
<span data-ttu-id="07403-106">A **New-AzContainerServiceConfig** parancsmag létrehoz egy helyi konfigurációs objektumot egy tároló szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="07403-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="07403-107">Ezt az objektumot a New-AzContainerService parancsmaggal hozhatja létre tároló szolgáltatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="07403-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="07403-108">Példák</span><span class="sxs-lookup"><span data-stu-id="07403-108">EXAMPLES</span></span>

### <span data-ttu-id="07403-109">Példa 1: tároló szolgáltatás konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="07403-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="07403-110">Ez a parancs létrehoz egy tárolót, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="07403-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="07403-111">A parancs a tároló szolgáltatás konfigurációjának különféle beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="07403-112">A parancs átadja a konfigurációs objektumot a Add-AzContainerServiceAgentPoolProfile parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="07403-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="07403-113">Ez a parancsmag egy Agent Pool-profilt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="07403-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="07403-114">Adja meg az objektumot $Container a **New-AzContainerService** *ContainerService* paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="07403-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="07403-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07403-115">PARAMETERS</span></span>

### <span data-ttu-id="07403-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="07403-116">-AdminUsername</span></span>
<span data-ttu-id="07403-117">A Linux-alapú tároló szolgáltatáshoz használt rendszergazdai fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="07403-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="07403-118">-AgentPoolProfile</span></span>
<span data-ttu-id="07403-119">A tároló szolgáltatáshoz tartozó Agent Pool-profil objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="07403-120">Profil hozzáadása a Add-AzContainerServiceAgentPoolProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="07403-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="07403-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="07403-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="07403-122">Az egyéni profil Orchestrator adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="07403-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07403-123">-DefaultProfile</span></span>
<span data-ttu-id="07403-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07403-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07403-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="07403-125">-Location</span></span>
<span data-ttu-id="07403-126">A tároló szolgáltatás létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="07403-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="07403-127">-MasterCount</span></span>
<span data-ttu-id="07403-128">A létrehozandó fő virtuális gépek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="07403-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="07403-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="07403-130">A fő virtuális gép DNS-előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="07403-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="07403-131">-OrchestratorType</span></span>
<span data-ttu-id="07403-132">A tároló szolgáltatás Orchestrator típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="07403-133">A paraméter elfogadható értékei a következők: DCOS és raj.</span><span class="sxs-lookup"><span data-stu-id="07403-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="07403-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="07403-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="07403-135">A fő profil ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="07403-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="07403-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="07403-137">A fő profil titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="07403-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="07403-138">-SshPublicKey</span></span>
<span data-ttu-id="07403-139">A Linux-alapú tároló szolgáltatás SSH-beli nyilvános kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="07403-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="07403-140">-Tag</span></span>
<span data-ttu-id="07403-141">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="07403-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="07403-142">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="07403-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="07403-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="07403-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="07403-144">Azt jelzi, hogy ez a konfiguráció engedélyezi-e a diagnosztikát a tároló szolgáltatás virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="07403-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="07403-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="07403-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="07403-146">Megadja a Windows operációs rendszert használó tároló-szolgáltatás rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="07403-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="07403-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="07403-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="07403-148">A Windows operációs rendszert használó tároló szolgáltatás rendszergazdai felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07403-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="07403-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07403-149">-Confirm</span></span>
<span data-ttu-id="07403-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07403-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07403-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07403-151">-WhatIf</span></span>
<span data-ttu-id="07403-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07403-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07403-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07403-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07403-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07403-154">CommonParameters</span></span>
<span data-ttu-id="07403-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07403-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07403-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07403-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07403-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07403-157">INPUTS</span></span>

### <span data-ttu-id="07403-158">System. String</span><span class="sxs-lookup"><span data-stu-id="07403-158">System.String</span></span>

### <span data-ttu-id="07403-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="07403-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="07403-160">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="07403-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="07403-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="07403-161">System.Int32</span></span>

### <span data-ttu-id="07403-162">Microsoft. Azure. Management. számítás. models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="07403-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="07403-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="07403-163">System.String[]</span></span>

### <span data-ttu-id="07403-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07403-164">System.Boolean</span></span>

## <span data-ttu-id="07403-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07403-165">OUTPUTS</span></span>

### <span data-ttu-id="07403-166">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="07403-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="07403-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07403-167">NOTES</span></span>

## <span data-ttu-id="07403-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07403-168">RELATED LINKS</span></span>

[<span data-ttu-id="07403-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="07403-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="07403-170">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="07403-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
