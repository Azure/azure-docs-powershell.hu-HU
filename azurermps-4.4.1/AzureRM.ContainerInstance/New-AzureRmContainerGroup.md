---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501920"
---
# <span data-ttu-id="29c5e-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="29c5e-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="29c5e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="29c5e-103">Tároló csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="29c5e-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29c5e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29c5e-104">SYNTAX</span></span>

### <span data-ttu-id="29c5e-105">CreateContainerGroupBaseParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29c5e-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c5e-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="29c5e-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c5e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29c5e-107">DESCRIPTION</span></span>
<span data-ttu-id="29c5e-108">A **New-AzureRmContainerGroup** parancsmagok tároló csoportot hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="29c5e-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="29c5e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29c5e-109">EXAMPLES</span></span>

### <span data-ttu-id="29c5e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29c5e-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="29c5e-111">Ez a parancs létrehoz egy tároló csoportot a legújabb Nginx képek segítségével, és nyilvános IP-címet kér a 8000-as port megnyitásával.</span><span class="sxs-lookup"><span data-stu-id="29c5e-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="29c5e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="29c5e-112">Example 2</span></span>
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
```

<span data-ttu-id="29c5e-113">Ez a parancs létrehoz egy tároló csoportot, és egy egyéni parancsfájlt futtat a tárolón belül.</span><span class="sxs-lookup"><span data-stu-id="29c5e-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="29c5e-114">3. példa: tároló-csoport létrehozása az Azure Container beállításjegyzékben lévő képpel</span><span class="sxs-lookup"><span data-stu-id="29c5e-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
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
```

<span data-ttu-id="29c5e-115">Ezzel a paranccsal létrehoz egy tároló csoportot egy Nginx képfájlból az Azure Container registry-ben.</span><span class="sxs-lookup"><span data-stu-id="29c5e-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="29c5e-116">Példa 4: a Container-csoport létrehozása kép használatával az egyéni tároló képnyilvántartóban</span><span class="sxs-lookup"><span data-stu-id="29c5e-116">Example 4: Creates a container group using image in custom container image registry</span></span>
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
```

<span data-ttu-id="29c5e-117">Ez a parancs létrehoz egy tároló csoportot egy egyéni tároló képnyilvántartóból származó egyéni képpel.</span><span class="sxs-lookup"><span data-stu-id="29c5e-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="29c5e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29c5e-118">PARAMETERS</span></span>

### <span data-ttu-id="29c5e-119">-Command</span><span class="sxs-lookup"><span data-stu-id="29c5e-119">-Command</span></span>
<span data-ttu-id="29c5e-120">A tárolóban futtatandó parancs.</span><span class="sxs-lookup"><span data-stu-id="29c5e-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="29c5e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29c5e-121">-Confirm</span></span>
<span data-ttu-id="29c5e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29c5e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c5e-123">-CPU</span><span class="sxs-lookup"><span data-stu-id="29c5e-123">-Cpu</span></span>
<span data-ttu-id="29c5e-124">A szükséges CPU-magok.</span><span class="sxs-lookup"><span data-stu-id="29c5e-124">The required CPU cores.</span></span>
<span data-ttu-id="29c5e-125">Alapértelmezett: 1</span><span class="sxs-lookup"><span data-stu-id="29c5e-125">Default: 1</span></span>

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

### <span data-ttu-id="29c5e-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="29c5e-126">-EnvironmentVariable</span></span>
<span data-ttu-id="29c5e-127">A tároló környezeti változói</span><span class="sxs-lookup"><span data-stu-id="29c5e-127">The container environment variables.</span></span>

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

### <span data-ttu-id="29c5e-128">-Kép</span><span class="sxs-lookup"><span data-stu-id="29c5e-128">-Image</span></span>
<span data-ttu-id="29c5e-129">A tároló képe.</span><span class="sxs-lookup"><span data-stu-id="29c5e-129">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c5e-130">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="29c5e-130">-IpAddressType</span></span>
<span data-ttu-id="29c5e-131">Az IP-cím típusa.</span><span class="sxs-lookup"><span data-stu-id="29c5e-131">The IP address type.</span></span>

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

### <span data-ttu-id="29c5e-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="29c5e-132">-Location</span></span>
<span data-ttu-id="29c5e-133">A tároló csoport helye.</span><span class="sxs-lookup"><span data-stu-id="29c5e-133">The container group Location.</span></span>
<span data-ttu-id="29c5e-134">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="29c5e-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="29c5e-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="29c5e-135">-MemoryInGB</span></span>
<span data-ttu-id="29c5e-136">A szükséges memória GB-ban.</span><span class="sxs-lookup"><span data-stu-id="29c5e-136">The required memory in GB.</span></span>
<span data-ttu-id="29c5e-137">Alapértelmezett: 1,5</span><span class="sxs-lookup"><span data-stu-id="29c5e-137">Default: 1.5</span></span>

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

### <span data-ttu-id="29c5e-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29c5e-138">-Name</span></span>
<span data-ttu-id="29c5e-139">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="29c5e-139">The container group name.</span></span>

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

### <span data-ttu-id="29c5e-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="29c5e-140">-OsType</span></span>
<span data-ttu-id="29c5e-141">A tároló operációs rendszer típusa</span><span class="sxs-lookup"><span data-stu-id="29c5e-141">The container OS type.</span></span>
<span data-ttu-id="29c5e-142">Alapértelmezett: Linux</span><span class="sxs-lookup"><span data-stu-id="29c5e-142">Default: Linux</span></span>

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

### <span data-ttu-id="29c5e-143">-Port</span><span class="sxs-lookup"><span data-stu-id="29c5e-143">-Port</span></span>
<span data-ttu-id="29c5e-144">A megnyitni kívánt port.</span><span class="sxs-lookup"><span data-stu-id="29c5e-144">The port to open.</span></span>
<span data-ttu-id="29c5e-145">Alapértelmezett: 80</span><span class="sxs-lookup"><span data-stu-id="29c5e-145">Default: 80</span></span>

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

### <span data-ttu-id="29c5e-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="29c5e-146">-RegistryCredential</span></span>
<span data-ttu-id="29c5e-147">Az egyéni tároló rendszerleíróadatbázis-hitelesítő adatai</span><span class="sxs-lookup"><span data-stu-id="29c5e-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c5e-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="29c5e-148">-RegistryServerDomain</span></span>
<span data-ttu-id="29c5e-149">Az egyéni tároló rendszerleíróadatbázis-bejelentkezési kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="29c5e-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c5e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c5e-150">-ResourceGroupName</span></span>
<span data-ttu-id="29c5e-151">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="29c5e-151">The resource group name.</span></span>

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

### <span data-ttu-id="29c5e-152">-Címke</span><span class="sxs-lookup"><span data-stu-id="29c5e-152">-Tag</span></span>
<span data-ttu-id="29c5e-153">{{Kitöltési címke leírása}}</span><span class="sxs-lookup"><span data-stu-id="29c5e-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="29c5e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c5e-154">-WhatIf</span></span>
<span data-ttu-id="29c5e-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29c5e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c5e-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29c5e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c5e-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c5e-157">-DefaultProfile</span></span>
<span data-ttu-id="29c5e-158">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29c5e-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29c5e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c5e-159">CommonParameters</span></span>
<span data-ttu-id="29c5e-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29c5e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c5e-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c5e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c5e-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29c5e-162">INPUTS</span></span>

### <span data-ttu-id="29c5e-163">System. String</span><span class="sxs-lookup"><span data-stu-id="29c5e-163">System.String</span></span>
<span data-ttu-id="29c5e-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="29c5e-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="29c5e-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29c5e-165">OUTPUTS</span></span>

### <span data-ttu-id="29c5e-166">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="29c5e-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="29c5e-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29c5e-167">NOTES</span></span>

## <span data-ttu-id="29c5e-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29c5e-168">RELATED LINKS</span></span>

