---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 1823759b72bdb3162164068732f3a8201fcfb589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492828"
---
# <span data-ttu-id="4ceea-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4ceea-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="4ceea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ceea-102">SYNOPSIS</span></span>
<span data-ttu-id="4ceea-103">Tároló csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4ceea-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ceea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ceea-104">SYNTAX</span></span>

### <span data-ttu-id="4ceea-105">CreateContainerGroupBaseParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ceea-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ceea-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="4ceea-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ceea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ceea-107">DESCRIPTION</span></span>
<span data-ttu-id="4ceea-108">A **New-AzureRmContainerGroup** parancsmagok tároló csoportot hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="4ceea-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="4ceea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4ceea-109">EXAMPLES</span></span>

### <span data-ttu-id="4ceea-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ceea-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="4ceea-111">Ez a parancs létrehoz egy tároló csoportot a legújabb Nginx képek segítségével, és nyilvános IP-címet kér a 8000-as port megnyitásával.</span><span class="sxs-lookup"><span data-stu-id="4ceea-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="4ceea-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="4ceea-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="4ceea-113">Ez a parancs létrehoz egy tároló csoportot, és egy egyéni parancsfájlt futtat a tárolón belül.</span><span class="sxs-lookup"><span data-stu-id="4ceea-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="4ceea-114">3. példa: a befejezésre kerülő tároló csoportot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4ceea-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="4ceea-115">Ez a parancs létrehoz egy tároló csoportot, amely a "helló" és a leállást nyomtatja.</span><span class="sxs-lookup"><span data-stu-id="4ceea-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="4ceea-116">4. példa: tároló-csoport létrehozása az Azure Container beállításjegyzékben lévő képpel</span><span class="sxs-lookup"><span data-stu-id="4ceea-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="4ceea-117">Ezzel a paranccsal létrehoz egy tároló csoportot egy Nginx képfájlból az Azure Container registry-ben.</span><span class="sxs-lookup"><span data-stu-id="4ceea-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="4ceea-118">Példa 5: a Container-csoport létrehozása kép használatával az egyéni tároló képnyilvántartásban</span><span class="sxs-lookup"><span data-stu-id="4ceea-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="4ceea-119">Ez a parancs létrehoz egy tároló csoportot egy egyéni tároló képnyilvántartóból származó egyéni képpel.</span><span class="sxs-lookup"><span data-stu-id="4ceea-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="4ceea-120">6. példa: az Azure-fájlok csatlakoztatására szolgáló tároló csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="4ceea-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="4ceea-121">Ez a parancs létrehoz egy tároló csoportot, amely a megadott Azure-fájlmegosztás csatlakoztatását tartalmazza `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="4ceea-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="4ceea-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ceea-122">PARAMETERS</span></span>

### <span data-ttu-id="4ceea-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4ceea-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="4ceea-124">Az Azure-fájlmegosztás tárolási fiókjának hitelesítő adatai, ahol a Felhasználónév a tárolási fiók neve, a kulcs pedig a tárolási fiók kulcsa.</span><span class="sxs-lookup"><span data-stu-id="4ceea-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ceea-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="4ceea-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="4ceea-126">Az Azure-fájl kötetének csatlakozási útvonala.</span><span class="sxs-lookup"><span data-stu-id="4ceea-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ceea-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="4ceea-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="4ceea-128">A Mount Azure-fájl megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="4ceea-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ceea-129">-Command</span><span class="sxs-lookup"><span data-stu-id="4ceea-129">-Command</span></span>
<span data-ttu-id="4ceea-130">A tárolóban futtatandó parancs.</span><span class="sxs-lookup"><span data-stu-id="4ceea-130">The command to run in the container.</span></span>

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

### <span data-ttu-id="4ceea-131">-CPU</span><span class="sxs-lookup"><span data-stu-id="4ceea-131">-Cpu</span></span>
<span data-ttu-id="4ceea-132">A szükséges CPU-magok.</span><span class="sxs-lookup"><span data-stu-id="4ceea-132">The required CPU cores.</span></span>
<span data-ttu-id="4ceea-133">Alapértelmezett: 1</span><span class="sxs-lookup"><span data-stu-id="4ceea-133">Default: 1</span></span>

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

### <span data-ttu-id="4ceea-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ceea-134">-DefaultProfile</span></span>
<span data-ttu-id="4ceea-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ceea-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ceea-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="4ceea-136">-DnsNameLabel</span></span>
<span data-ttu-id="4ceea-137">Az IP-cím DNS-név címkéje.</span><span class="sxs-lookup"><span data-stu-id="4ceea-137">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="4ceea-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="4ceea-138">-EnvironmentVariable</span></span>
<span data-ttu-id="4ceea-139">A tároló környezeti változói</span><span class="sxs-lookup"><span data-stu-id="4ceea-139">The container environment variables.</span></span>

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

### <span data-ttu-id="4ceea-140">-Kép</span><span class="sxs-lookup"><span data-stu-id="4ceea-140">-Image</span></span>
<span data-ttu-id="4ceea-141">A tároló képe.</span><span class="sxs-lookup"><span data-stu-id="4ceea-141">The container image.</span></span>

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

### <span data-ttu-id="4ceea-142">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="4ceea-142">-IpAddressType</span></span>
<span data-ttu-id="4ceea-143">Az IP-cím típusa.</span><span class="sxs-lookup"><span data-stu-id="4ceea-143">The IP address type.</span></span>

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

### <span data-ttu-id="4ceea-144">-Hely</span><span class="sxs-lookup"><span data-stu-id="4ceea-144">-Location</span></span>
<span data-ttu-id="4ceea-145">A tároló csoport helye.</span><span class="sxs-lookup"><span data-stu-id="4ceea-145">The container group Location.</span></span>
<span data-ttu-id="4ceea-146">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="4ceea-146">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="4ceea-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="4ceea-147">-MemoryInGB</span></span>
<span data-ttu-id="4ceea-148">A szükséges memória GB-ban.</span><span class="sxs-lookup"><span data-stu-id="4ceea-148">The required memory in GB.</span></span>
<span data-ttu-id="4ceea-149">Alapértelmezett: 1,5</span><span class="sxs-lookup"><span data-stu-id="4ceea-149">Default: 1.5</span></span>

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

### <span data-ttu-id="4ceea-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ceea-150">-Name</span></span>
<span data-ttu-id="4ceea-151">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4ceea-151">The container group name.</span></span>

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

### <span data-ttu-id="4ceea-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="4ceea-152">-OsType</span></span>
<span data-ttu-id="4ceea-153">A tároló operációs rendszer típusa</span><span class="sxs-lookup"><span data-stu-id="4ceea-153">The container OS type.</span></span>
<span data-ttu-id="4ceea-154">Alapértelmezett: Linux</span><span class="sxs-lookup"><span data-stu-id="4ceea-154">Default: Linux</span></span>

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

### <span data-ttu-id="4ceea-155">-Port</span><span class="sxs-lookup"><span data-stu-id="4ceea-155">-Port</span></span>
<span data-ttu-id="4ceea-156">A megnyitni kívánt port (ok)</span><span class="sxs-lookup"><span data-stu-id="4ceea-156">The port(s) to open.</span></span> <span data-ttu-id="4ceea-157">Alapértelmezett: [80]</span><span class="sxs-lookup"><span data-stu-id="4ceea-157">Default: [80]</span></span>

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

### <span data-ttu-id="4ceea-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4ceea-158">-RegistryCredential</span></span>
<span data-ttu-id="4ceea-159">Az egyéni tároló rendszerleíróadatbázis-hitelesítő adatai</span><span class="sxs-lookup"><span data-stu-id="4ceea-159">The custom container registry credential.</span></span>

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

### <span data-ttu-id="4ceea-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="4ceea-160">-RegistryServerDomain</span></span>
<span data-ttu-id="4ceea-161">Az egyéni tároló rendszerleíróadatbázis-bejelentkezési kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="4ceea-161">The custom container registry login server.</span></span>

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

### <span data-ttu-id="4ceea-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ceea-162">-ResourceGroupName</span></span>
<span data-ttu-id="4ceea-163">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4ceea-163">The resource group name.</span></span>

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

### <span data-ttu-id="4ceea-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="4ceea-164">-RestartPolicy</span></span>
<span data-ttu-id="4ceea-165">A tároló újraindítása házirend.</span><span class="sxs-lookup"><span data-stu-id="4ceea-165">The container restart policy.</span></span> <span data-ttu-id="4ceea-166">Alapértelmezett: mindig</span><span class="sxs-lookup"><span data-stu-id="4ceea-166">Default: Always</span></span>

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

### <span data-ttu-id="4ceea-167">-Címke</span><span class="sxs-lookup"><span data-stu-id="4ceea-167">-Tag</span></span>
<span data-ttu-id="4ceea-168">{{Kitöltési címke leírása}}</span><span class="sxs-lookup"><span data-stu-id="4ceea-168">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="4ceea-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ceea-169">-Confirm</span></span>
<span data-ttu-id="4ceea-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ceea-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ceea-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ceea-171">-WhatIf</span></span>
<span data-ttu-id="4ceea-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ceea-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ceea-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ceea-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ceea-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ceea-174">CommonParameters</span></span>
<span data-ttu-id="4ceea-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ceea-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ceea-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ceea-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ceea-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ceea-177">INPUTS</span></span>

### <span data-ttu-id="4ceea-178">System. String</span><span class="sxs-lookup"><span data-stu-id="4ceea-178">System.String</span></span>

### <span data-ttu-id="4ceea-179">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ceea-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ceea-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ceea-180">OUTPUTS</span></span>

### <span data-ttu-id="4ceea-181">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4ceea-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="4ceea-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ceea-182">NOTES</span></span>

## <span data-ttu-id="4ceea-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ceea-183">RELATED LINKS</span></span>
