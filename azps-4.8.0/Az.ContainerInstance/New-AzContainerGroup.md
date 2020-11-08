---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024094"
---
# <span data-ttu-id="c40b2-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c40b2-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="c40b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c40b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c40b2-103">Tároló csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c40b2-103">Creates a container group.</span></span>

## <span data-ttu-id="c40b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c40b2-104">SYNTAX</span></span>

### <span data-ttu-id="c40b2-105">CreateContainerGroupBaseParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c40b2-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40b2-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="c40b2-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40b2-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="c40b2-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40b2-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c40b2-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c40b2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c40b2-109">DESCRIPTION</span></span>
<span data-ttu-id="c40b2-110">A **New-AzContainerGroup** parancsmagok tároló csoportot hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="c40b2-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="c40b2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c40b2-111">EXAMPLES</span></span>

### <span data-ttu-id="c40b2-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c40b2-112">Example 1</span></span>
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

<span data-ttu-id="c40b2-113">Ez a parancs létrehoz egy tároló csoportot a legújabb Nginx képek segítségével, és nyilvános IP-címet kér a 8000-as port megnyitásával.</span><span class="sxs-lookup"><span data-stu-id="c40b2-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="c40b2-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c40b2-114">Example 2</span></span>
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

<span data-ttu-id="c40b2-115">Ez a parancs létrehoz egy tároló csoportot, és egy egyéni parancsfájlt futtat a tárolón belül.</span><span class="sxs-lookup"><span data-stu-id="c40b2-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="c40b2-116">3. példa: a befejezésre kerülő tároló csoportot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c40b2-116">Example 3: Creates a run-to-completion container group.</span></span>
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

<span data-ttu-id="c40b2-117">Ez a parancs létrehoz egy tároló csoportot, amely a "helló" és a leállást nyomtatja.</span><span class="sxs-lookup"><span data-stu-id="c40b2-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="c40b2-118">4. példa: tároló-csoport létrehozása az Azure Container beállításjegyzékben lévő képpel</span><span class="sxs-lookup"><span data-stu-id="c40b2-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
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

<span data-ttu-id="c40b2-119">Ezzel a paranccsal létrehoz egy tároló csoportot egy Nginx képfájlból az Azure Container registry-ben.</span><span class="sxs-lookup"><span data-stu-id="c40b2-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="c40b2-120">Példa 5: a Container-csoport létrehozása kép használatával az egyéni tároló képnyilvántartásban</span><span class="sxs-lookup"><span data-stu-id="c40b2-120">Example 5: Creates a container group using image in custom container image registry</span></span>
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

<span data-ttu-id="c40b2-121">Ez a parancs létrehoz egy tároló csoportot egy egyéni tároló képnyilvántartóból származó egyéni képpel.</span><span class="sxs-lookup"><span data-stu-id="c40b2-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="c40b2-122">6. példa: az Azure-fájlok csatlakoztatására szolgáló tároló csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="c40b2-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
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

<span data-ttu-id="c40b2-123">Ez a parancs létrehoz egy tároló csoportot, amely a megadott Azure-fájlmegosztás csatlakoztatását tartalmazza `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="c40b2-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="c40b2-124">7. példa</span><span class="sxs-lookup"><span data-stu-id="c40b2-124">Example 7</span></span>
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

<span data-ttu-id="c40b2-125">Ez a parancs létrehoz egy tároló csoportot a rendszerhez rendelt identitással a legújabb Nginx képen, és nyilvános IP-címet kér a 8000-as port megnyitásával.</span><span class="sxs-lookup"><span data-stu-id="c40b2-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="c40b2-126">8. példa</span><span class="sxs-lookup"><span data-stu-id="c40b2-126">Example 8</span></span>
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

<span data-ttu-id="c40b2-127">Ez a parancs létrehoz egy tároló csoportot a rendszer kiosztott és a felhasználó által kiosztott identitással a legújabb Nginx képen, és a 8000-as port megnyitásával nyilvános IP-címet kér.</span><span class="sxs-lookup"><span data-stu-id="c40b2-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="c40b2-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c40b2-128">PARAMETERS</span></span>

### <span data-ttu-id="c40b2-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c40b2-129">-AssignIdentity</span></span>
<span data-ttu-id="c40b2-130">A rendszer által kiosztott identitás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="c40b2-130">Enable system assigned identity</span></span>

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

### <span data-ttu-id="c40b2-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c40b2-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="c40b2-132">Az Azure-fájlmegosztás tárolási fiókjának hitelesítő adatai, ahol a Felhasználónév a tárolási fiók neve, a kulcs pedig a tárolási fiók kulcsa.</span><span class="sxs-lookup"><span data-stu-id="c40b2-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

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

### <span data-ttu-id="c40b2-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="c40b2-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="c40b2-134">Az Azure-fájl kötetének csatlakozási útvonala.</span><span class="sxs-lookup"><span data-stu-id="c40b2-134">The mount path for the Azure File volume.</span></span>

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

### <span data-ttu-id="c40b2-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="c40b2-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="c40b2-136">A Mount Azure-fájl megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="c40b2-136">The name of the Azure File share to mount.</span></span>

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

### <span data-ttu-id="c40b2-137">-Command</span><span class="sxs-lookup"><span data-stu-id="c40b2-137">-Command</span></span>
<span data-ttu-id="c40b2-138">A tárolóban futtatandó parancs.</span><span class="sxs-lookup"><span data-stu-id="c40b2-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="c40b2-139">-CPU</span><span class="sxs-lookup"><span data-stu-id="c40b2-139">-Cpu</span></span>
<span data-ttu-id="c40b2-140">A szükséges CPU-magok.</span><span class="sxs-lookup"><span data-stu-id="c40b2-140">The required CPU cores.</span></span>
<span data-ttu-id="c40b2-141">Alapértelmezett: 1</span><span class="sxs-lookup"><span data-stu-id="c40b2-141">Default: 1</span></span>

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

### <span data-ttu-id="c40b2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40b2-142">-DefaultProfile</span></span>
<span data-ttu-id="c40b2-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c40b2-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c40b2-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="c40b2-144">-DnsNameLabel</span></span>
<span data-ttu-id="c40b2-145">Az IP-cím DNS-név címkéje.</span><span class="sxs-lookup"><span data-stu-id="c40b2-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="c40b2-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="c40b2-146">-EnvironmentVariable</span></span>
<span data-ttu-id="c40b2-147">A tároló környezeti változói</span><span class="sxs-lookup"><span data-stu-id="c40b2-147">The container environment variables.</span></span>

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

### <span data-ttu-id="c40b2-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="c40b2-148">-IdentityId</span></span>
<span data-ttu-id="c40b2-149">A felhasználó által kiosztott azonosítók azonosítói</span><span class="sxs-lookup"><span data-stu-id="c40b2-149">The user assigned identity IDs</span></span>

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

### <span data-ttu-id="c40b2-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c40b2-150">-IdentityType</span></span>
<span data-ttu-id="c40b2-151">A felügyelt identitás típusa</span><span class="sxs-lookup"><span data-stu-id="c40b2-151">The managed identity type</span></span>

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

### <span data-ttu-id="c40b2-152">-Kép</span><span class="sxs-lookup"><span data-stu-id="c40b2-152">-Image</span></span>
<span data-ttu-id="c40b2-153">A tároló képe.</span><span class="sxs-lookup"><span data-stu-id="c40b2-153">The container image.</span></span>

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

### <span data-ttu-id="c40b2-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="c40b2-154">-IpAddressType</span></span>
<span data-ttu-id="c40b2-155">Az IP-cím típusa.</span><span class="sxs-lookup"><span data-stu-id="c40b2-155">The IP address type.</span></span>

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

### <span data-ttu-id="c40b2-156">-Hely</span><span class="sxs-lookup"><span data-stu-id="c40b2-156">-Location</span></span>
<span data-ttu-id="c40b2-157">A tároló csoport helye.</span><span class="sxs-lookup"><span data-stu-id="c40b2-157">The container group Location.</span></span>
<span data-ttu-id="c40b2-158">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="c40b2-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="c40b2-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="c40b2-159">-MemoryInGB</span></span>
<span data-ttu-id="c40b2-160">A szükséges memória GB-ban.</span><span class="sxs-lookup"><span data-stu-id="c40b2-160">The required memory in GB.</span></span>
<span data-ttu-id="c40b2-161">Alapértelmezett: 1,5</span><span class="sxs-lookup"><span data-stu-id="c40b2-161">Default: 1.5</span></span>

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

### <span data-ttu-id="c40b2-162">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c40b2-162">-Name</span></span>
<span data-ttu-id="c40b2-163">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c40b2-163">The container group name.</span></span>

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

### <span data-ttu-id="c40b2-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="c40b2-164">-OsType</span></span>
<span data-ttu-id="c40b2-165">A tároló operációs rendszer típusa</span><span class="sxs-lookup"><span data-stu-id="c40b2-165">The container OS type.</span></span>
<span data-ttu-id="c40b2-166">Alapértelmezett: Linux</span><span class="sxs-lookup"><span data-stu-id="c40b2-166">Default: Linux</span></span>

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

### <span data-ttu-id="c40b2-167">-Port</span><span class="sxs-lookup"><span data-stu-id="c40b2-167">-Port</span></span>
<span data-ttu-id="c40b2-168">A megnyitni kívánt port (ok)</span><span class="sxs-lookup"><span data-stu-id="c40b2-168">The port(s) to open.</span></span> <span data-ttu-id="c40b2-169">Alapértelmezett: [80]</span><span class="sxs-lookup"><span data-stu-id="c40b2-169">Default: [80]</span></span>

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

### <span data-ttu-id="c40b2-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c40b2-170">-RegistryCredential</span></span>
<span data-ttu-id="c40b2-171">Az egyéni tároló rendszerleíróadatbázis-hitelesítő adatai</span><span class="sxs-lookup"><span data-stu-id="c40b2-171">The custom container registry credential.</span></span>

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

### <span data-ttu-id="c40b2-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="c40b2-172">-RegistryServerDomain</span></span>
<span data-ttu-id="c40b2-173">Az egyéni tároló rendszerleíróadatbázis-bejelentkezési kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="c40b2-173">The custom container registry login server.</span></span>

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

### <span data-ttu-id="c40b2-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c40b2-174">-ResourceGroupName</span></span>
<span data-ttu-id="c40b2-175">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c40b2-175">The resource group name.</span></span>

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

### <span data-ttu-id="c40b2-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="c40b2-176">-RestartPolicy</span></span>
<span data-ttu-id="c40b2-177">A tároló újraindítása házirend.</span><span class="sxs-lookup"><span data-stu-id="c40b2-177">The container restart policy.</span></span> <span data-ttu-id="c40b2-178">Alapértelmezett: mindig</span><span class="sxs-lookup"><span data-stu-id="c40b2-178">Default: Always</span></span>

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

### <span data-ttu-id="c40b2-179">-Címke</span><span class="sxs-lookup"><span data-stu-id="c40b2-179">-Tag</span></span>
<span data-ttu-id="c40b2-180">{{Kitöltési címke leírása}}</span><span class="sxs-lookup"><span data-stu-id="c40b2-180">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="c40b2-181">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c40b2-181">-Confirm</span></span>
<span data-ttu-id="c40b2-182">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c40b2-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c40b2-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c40b2-183">-WhatIf</span></span>
<span data-ttu-id="c40b2-184">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c40b2-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c40b2-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c40b2-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c40b2-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40b2-186">CommonParameters</span></span>
<span data-ttu-id="c40b2-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c40b2-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40b2-188">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c40b2-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40b2-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c40b2-189">INPUTS</span></span>

### <span data-ttu-id="c40b2-190">System. String</span><span class="sxs-lookup"><span data-stu-id="c40b2-190">System.String</span></span>

### <span data-ttu-id="c40b2-191">System. string []</span><span class="sxs-lookup"><span data-stu-id="c40b2-191">System.String[]</span></span>

### <span data-ttu-id="c40b2-192">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c40b2-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c40b2-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c40b2-193">OUTPUTS</span></span>

### <span data-ttu-id="c40b2-194">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c40b2-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="c40b2-195">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c40b2-195">NOTES</span></span>

## <span data-ttu-id="c40b2-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c40b2-196">RELATED LINKS</span></span>
