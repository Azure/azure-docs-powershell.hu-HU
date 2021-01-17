---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349253"
---
# <span data-ttu-id="914a8-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="914a8-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="914a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="914a8-102">SYNOPSIS</span></span>
<span data-ttu-id="914a8-103">Helyi konfigurációs objektumot hoz létre egy tárolószolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="914a8-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="914a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="914a8-104">SYNTAX</span></span>

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

## <span data-ttu-id="914a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="914a8-105">DESCRIPTION</span></span>
<span data-ttu-id="914a8-106">A **New-AzContainerServiceConfig** parancsmag helyi konfigurációs objektumot hoz létre egy tárolószolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="914a8-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="914a8-107">Adja ezt az objektumot a New-AzContainerService parancsmagnak egy tárolószolgáltatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="914a8-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="914a8-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="914a8-108">EXAMPLES</span></span>

### <span data-ttu-id="914a8-109">1. példa: Tárolószolgáltatás-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="914a8-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="914a8-110">Ez a parancs létrehoz egy tárolót, majd a $Container tárolja.</span><span class="sxs-lookup"><span data-stu-id="914a8-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="914a8-111">A parancs a tárolószolgáltatás-konfiguráció különféle beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="914a8-112">A parancs a folyamat műveleti Add-AzContainerServiceAgentPoolProfile keresztül átadja a konfigurációs objektumot a Add-AzContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="914a8-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="914a8-113">Ez a parancsmag hozzáad egy ügynökkészlet-profilt.</span><span class="sxs-lookup"><span data-stu-id="914a8-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="914a8-114">Adja meg az $Container a **New-AzContainerService** *ContainerService* paraméterének megfelelő objektumot.</span><span class="sxs-lookup"><span data-stu-id="914a8-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="914a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="914a8-115">PARAMETERS</span></span>

### <span data-ttu-id="914a8-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="914a8-116">-AdminUsername</span></span>
<span data-ttu-id="914a8-117">A Linux-alapú tárolószolgáltatáshoz használt rendszergazdai fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="914a8-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="914a8-118">-AgentPoolProfile</span></span>
<span data-ttu-id="914a8-119">A tárolószolgáltatás ügynökkészlet-profilobjektumai tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="914a8-120">Profil hozzáadása a Add-AzContainerServiceAgentPoolProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="914a8-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="914a8-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="914a8-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="914a8-122">Az egyéni profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="914a8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="914a8-123">-DefaultProfile</span></span>
<span data-ttu-id="914a8-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="914a8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="914a8-125">-Location</span><span class="sxs-lookup"><span data-stu-id="914a8-125">-Location</span></span>
<span data-ttu-id="914a8-126">Azt a helyet adja meg, ahol létre kell hoznia a tárolószolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="914a8-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="914a8-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="914a8-127">-MasterCount</span></span>
<span data-ttu-id="914a8-128">A létrehozni szükséges fő virtuális gépek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="914a8-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="914a8-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="914a8-130">A virtuális főgép DNS-előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="914a8-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="914a8-131">-OrchestratorType</span></span>
<span data-ttu-id="914a8-132">Megadja a tárolószolgáltatáshoz a összehangoló típusát.</span><span class="sxs-lookup"><span data-stu-id="914a8-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="914a8-133">A paraméter elfogadható értékei a következőek: DCOS és Swarm.</span><span class="sxs-lookup"><span data-stu-id="914a8-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="914a8-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="914a8-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="914a8-135">A fő profil ügyfélazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="914a8-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="914a8-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="914a8-137">A fő profiltitkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="914a8-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="914a8-138">-SshPublicKey</span></span>
<span data-ttu-id="914a8-139">Egy Linux-alapú tárolószolgáltatás SSH nyilvános kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="914a8-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="914a8-140">-Tag</span></span>
<span data-ttu-id="914a8-141">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="914a8-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="914a8-142">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="914a8-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="914a8-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="914a8-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="914a8-144">Azt jelzi, hogy ez a konfiguráció engedélyezi-e a diagnosztika a tárolószolgáltatás virtuális gépét.</span><span class="sxs-lookup"><span data-stu-id="914a8-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="914a8-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="914a8-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="914a8-146">A Windows operációs rendszert használó tárolószolgáltatás rendszergazdai jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="914a8-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="914a8-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="914a8-148">A Windows operációs rendszert használó tárolószolgáltatás rendszergazdai felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="914a8-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="914a8-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="914a8-149">-Confirm</span></span>
<span data-ttu-id="914a8-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="914a8-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="914a8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="914a8-151">-WhatIf</span></span>
<span data-ttu-id="914a8-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="914a8-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="914a8-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="914a8-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="914a8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="914a8-154">CommonParameters</span></span>
<span data-ttu-id="914a8-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="914a8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="914a8-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="914a8-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="914a8-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="914a8-157">INPUTS</span></span>

### <span data-ttu-id="914a8-158">System.String</span><span class="sxs-lookup"><span data-stu-id="914a8-158">System.String</span></span>

### <span data-ttu-id="914a8-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="914a8-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="914a8-160">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="914a8-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="914a8-161">System.Int32</span><span class="sxs-lookup"><span data-stu-id="914a8-161">System.Int32</span></span>

### <span data-ttu-id="914a8-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span><span class="sxs-lookup"><span data-stu-id="914a8-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="914a8-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="914a8-163">System.String[]</span></span>

### <span data-ttu-id="914a8-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="914a8-164">System.Boolean</span></span>

## <span data-ttu-id="914a8-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="914a8-165">OUTPUTS</span></span>

### <span data-ttu-id="914a8-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="914a8-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="914a8-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="914a8-167">NOTES</span></span>

## <span data-ttu-id="914a8-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="914a8-168">RELATED LINKS</span></span>

[<span data-ttu-id="914a8-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="914a8-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="914a8-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="914a8-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
