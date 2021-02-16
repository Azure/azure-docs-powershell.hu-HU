---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148738"
---
# <span data-ttu-id="597ce-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="597ce-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="597ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="597ce-102">SYNOPSIS</span></span>
<span data-ttu-id="597ce-103">Tárolócsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="597ce-103">Creates a container group.</span></span>

## <span data-ttu-id="597ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="597ce-104">SYNTAX</span></span>

### <span data-ttu-id="597ce-105">CreateContainerGroupBaseParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="597ce-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="597ce-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="597ce-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="597ce-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="597ce-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="597ce-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="597ce-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="597ce-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="597ce-109">DESCRIPTION</span></span>
<span data-ttu-id="597ce-110">A **New-AzContainerGroup** parancsmagok egy tárolócsoportot hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="597ce-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="597ce-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="597ce-111">EXAMPLES</span></span>

### <span data-ttu-id="597ce-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="597ce-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="597ce-113">Ez a parancs a legújabb nginx-kép alapján létrehoz egy tárolócsoportot, és nyilvános IP-címet kér a 8000-es port megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="597ce-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="597ce-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="597ce-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="597ce-115">Ez a parancs egy tárolócsoportot hoz létre, és egy egyéni parancsfájlt futtat a tárolón belül.</span><span class="sxs-lookup"><span data-stu-id="597ce-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="597ce-116">3. példa: Futtatásig tartó tárolócsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="597ce-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="597ce-117">Ez a parancs létrehoz egy tárolócsoportot, amely kiírja a "hello" és a stops (hello) nyomatot.</span><span class="sxs-lookup"><span data-stu-id="597ce-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="597ce-118">4. példa: Tárolócsoportot hoz létre kép használatával az Azure Container Registry szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="597ce-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="597ce-119">Ez a parancs egy nginx-lemezképet használó tárolócsoportot hoz létre az Azure Container Registry szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="597ce-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="597ce-120">5. példa: Tárolócsoport létrehozása kép használatával az egyéni tárolókép beállításjegyzékében</span><span class="sxs-lookup"><span data-stu-id="597ce-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="597ce-121">Ez a parancs egyéni lemezkép használatával hoz létre egy tárolócsoportot egy egyéni tárolókép beállításjegyzékében.</span><span class="sxs-lookup"><span data-stu-id="597ce-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="597ce-122">6. példa: Létrehoz egy tárolócsoportot, amely az Azure-fájlkötetet csatlakoztatja</span><span class="sxs-lookup"><span data-stu-id="597ce-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name mycontainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountCredential $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="597ce-123">Ez a parancs létrehoz egy tárolócsoportot, amely a megadott Azure-fájlmegosztást `/mnt/azfile` csatlakoztatja.</span><span class="sxs-lookup"><span data-stu-id="597ce-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="597ce-124">7. példa</span><span class="sxs-lookup"><span data-stu-id="597ce-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="597ce-125">Ez a parancs létrehoz egy rendszerhez rendelt identitást tartalmazó tárolócsoportot a legújabb nginx-kép használatával, és nyilvános IP-címet kér a 8000-es port megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="597ce-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="597ce-126">8. példa</span><span class="sxs-lookup"><span data-stu-id="597ce-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="597ce-127">Ez a parancs egy olyan tárolócsoportot hoz létre, amely a legújabb nginx-kép alapján rendszerből és felhasználóhoz rendelt identitásból áll, és nyilvános IP-címet kér a 8000-es port megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="597ce-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="597ce-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="597ce-128">PARAMETERS</span></span>

### <span data-ttu-id="597ce-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="597ce-129">-AssignIdentity</span></span>
<span data-ttu-id="597ce-130">Rendszerhez rendelt identitás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="597ce-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="597ce-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="597ce-132">Az Azure-fájlmegosztáshoz tartozó tárfiók hitelesítő adatai, ahol a felhasználónév a tárfiók neve, a kulcs pedig a tárfiók kulcsa.</span><span class="sxs-lookup"><span data-stu-id="597ce-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="597ce-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="597ce-134">Az Azure-fájl hangerejének csatlakoztatási útvonala.</span><span class="sxs-lookup"><span data-stu-id="597ce-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="597ce-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="597ce-136">A csatlakoztatni kívánt Azure-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="597ce-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-137">-Command</span><span class="sxs-lookup"><span data-stu-id="597ce-137">-Command</span></span>
<span data-ttu-id="597ce-138">A tárolóban futtatandó parancs.</span><span class="sxs-lookup"><span data-stu-id="597ce-138">The command to run in the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-139">-Cpu</span><span class="sxs-lookup"><span data-stu-id="597ce-139">-Cpu</span></span>
<span data-ttu-id="597ce-140">A szükséges processzormagok.</span><span class="sxs-lookup"><span data-stu-id="597ce-140">The required CPU cores.</span></span>
<span data-ttu-id="597ce-141">Alapértelmezett: 1</span><span class="sxs-lookup"><span data-stu-id="597ce-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597ce-142">-DefaultProfile</span></span>
<span data-ttu-id="597ce-143">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="597ce-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="597ce-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="597ce-144">-DnsNameLabel</span></span>
<span data-ttu-id="597ce-145">Az IP-cím DNS-névfelirata.</span><span class="sxs-lookup"><span data-stu-id="597ce-145">The DNS name label for the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="597ce-146">-EnvironmentVariable</span></span>
<span data-ttu-id="597ce-147">A tárolókörnyezet változói.</span><span class="sxs-lookup"><span data-stu-id="597ce-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="597ce-148">-IdentityId</span></span>
<span data-ttu-id="597ce-149">A felhasználóhoz rendelt identitás-azonosítók</span><span class="sxs-lookup"><span data-stu-id="597ce-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="597ce-150">-IdentityType</span></span>
<span data-ttu-id="597ce-151">A felügyelt identitás típusa</span><span class="sxs-lookup"><span data-stu-id="597ce-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-152">-Image</span><span class="sxs-lookup"><span data-stu-id="597ce-152">-Image</span></span>
<span data-ttu-id="597ce-153">A tároló képe.</span><span class="sxs-lookup"><span data-stu-id="597ce-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="597ce-154">-IpAddressType</span></span>
<span data-ttu-id="597ce-155">Az IP-cím típusa.</span><span class="sxs-lookup"><span data-stu-id="597ce-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-156">-Location</span><span class="sxs-lookup"><span data-stu-id="597ce-156">-Location</span></span>
<span data-ttu-id="597ce-157">A Hely tárolócsoport.</span><span class="sxs-lookup"><span data-stu-id="597ce-157">The container group Location.</span></span>
<span data-ttu-id="597ce-158">Alapértelmezés szerint az erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="597ce-158">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="597ce-159">-MemoryInGB</span></span>
<span data-ttu-id="597ce-160">A szükséges memória GB-ban.</span><span class="sxs-lookup"><span data-stu-id="597ce-160">The required memory in GB.</span></span>
<span data-ttu-id="597ce-161">Alapértelmezett: 1,5</span><span class="sxs-lookup"><span data-stu-id="597ce-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-162">-Name</span><span class="sxs-lookup"><span data-stu-id="597ce-162">-Name</span></span>
<span data-ttu-id="597ce-163">A tárolócsoport neve.</span><span class="sxs-lookup"><span data-stu-id="597ce-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="597ce-164">-OsType</span></span>
<span data-ttu-id="597ce-165">A tároló operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="597ce-165">The container OS type.</span></span>
<span data-ttu-id="597ce-166">Alapértelmezett: Linux</span><span class="sxs-lookup"><span data-stu-id="597ce-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-167">-Port</span><span class="sxs-lookup"><span data-stu-id="597ce-167">-Port</span></span>
<span data-ttu-id="597ce-168">A megnyílik port(ak).</span><span class="sxs-lookup"><span data-stu-id="597ce-168">The port(s) to open.</span></span> <span data-ttu-id="597ce-169">Alapértelmezett: [80]</span><span class="sxs-lookup"><span data-stu-id="597ce-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="597ce-170">-RegistryCredential</span></span>
<span data-ttu-id="597ce-171">Az egyéni tároló beállításjegyzékének hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="597ce-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="597ce-172">-RegistryServerDomain</span></span>
<span data-ttu-id="597ce-173">Az egyéni tároló beállításjegyzékének bejelentkezési kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="597ce-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="597ce-174">-ResourceGroupName</span></span>
<span data-ttu-id="597ce-175">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="597ce-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="597ce-176">-RestartPolicy</span></span>
<span data-ttu-id="597ce-177">A tároló újraindítási házirende.</span><span class="sxs-lookup"><span data-stu-id="597ce-177">The container restart policy.</span></span> <span data-ttu-id="597ce-178">Alapértelmezett: Mindig</span><span class="sxs-lookup"><span data-stu-id="597ce-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="597ce-179">-Tag</span></span>
<span data-ttu-id="597ce-180">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="597ce-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="597ce-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="597ce-181">-Confirm</span></span>
<span data-ttu-id="597ce-182">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="597ce-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="597ce-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="597ce-183">-WhatIf</span></span>
<span data-ttu-id="597ce-184">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="597ce-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="597ce-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="597ce-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="597ce-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597ce-186">CommonParameters</span></span>
<span data-ttu-id="597ce-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597ce-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597ce-188">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="597ce-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597ce-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="597ce-189">INPUTS</span></span>

### <span data-ttu-id="597ce-190">System.String</span><span class="sxs-lookup"><span data-stu-id="597ce-190">System.String</span></span>

### <span data-ttu-id="597ce-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="597ce-191">System.String[]</span></span>

### <span data-ttu-id="597ce-192">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="597ce-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="597ce-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="597ce-193">OUTPUTS</span></span>

### <span data-ttu-id="597ce-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="597ce-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="597ce-195">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="597ce-195">NOTES</span></span>

## <span data-ttu-id="597ce-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="597ce-196">RELATED LINKS</span></span>
