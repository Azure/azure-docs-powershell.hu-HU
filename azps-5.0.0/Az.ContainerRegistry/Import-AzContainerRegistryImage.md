---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296384"
---
# <span data-ttu-id="cbdc4-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="cbdc4-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="cbdc4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdc4-103">Kép importálása nyilvános vagy Azure-webhelyről egy Azure Container-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="cbdc4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbdc4-104">SYNTAX</span></span>

### <span data-ttu-id="cbdc4-105">ImportImageByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbdc4-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbdc4-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="cbdc4-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbdc4-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="cbdc4-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbdc4-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="cbdc4-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbdc4-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbdc4-109">DESCRIPTION</span></span>
<span data-ttu-id="cbdc4-110">Kép importálása nyilvános vagy Azure-webhelyről egy Azure Container-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="cbdc4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cbdc4-111">EXAMPLES</span></span>

### <span data-ttu-id="cbdc4-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cbdc4-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="cbdc4-113">BusyBox importálása az ACR-ba</span><span class="sxs-lookup"><span data-stu-id="cbdc4-113">Import busybox to ACR.</span></span> <span data-ttu-id="cbdc4-114">Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="cbdc4-114">Note:</span></span> 
* <span data-ttu-id="cbdc4-115">a "tár/" szót fel kell venni a forrás képe előtt.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="cbdc4-116">"BusyBox: Latest" => "Library/BusyBox: Latest"</span><span class="sxs-lookup"><span data-stu-id="cbdc4-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="cbdc4-117">Hitelesítő adatokra van szükség, ha a forrás beállításjegyzéke nem érhető el nyilvánosan</span><span class="sxs-lookup"><span data-stu-id="cbdc4-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="cbdc4-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="cbdc4-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="cbdc4-119">Az ACR-ből az ACR-BusyBox importálhatja a forrást.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="cbdc4-120">Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="cbdc4-120">Note:</span></span> 
* <span data-ttu-id="cbdc4-121">Hitelesítő adatokra van szükség, ha a rendszergazdai felhasználó a forráskódot letiltotta.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="cbdc4-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbdc4-122">PARAMETERS</span></span>

### <span data-ttu-id="cbdc4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdc4-123">-DefaultProfile</span></span>
<span data-ttu-id="cbdc4-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbdc4-125">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="cbdc4-125">-Mode</span></span>
<span data-ttu-id="cbdc4-126">Ha az erő, minden meglévő cél-címke felülírható.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="cbdc4-127">Ha nincs ilyen, minden meglévő cél-címke sikertelen lesz a művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc4-128">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="cbdc4-128">-Password</span></span>
<span data-ttu-id="cbdc4-129">A forrás-nyilvántartóval való hitelesítéshez használt jelszó.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc4-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="cbdc4-130">-RegistryName</span></span>
<span data-ttu-id="cbdc4-131">A cél beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-131">Target registry name.</span></span>

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

### <span data-ttu-id="cbdc4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdc4-132">-ResourceGroupName</span></span>
<span data-ttu-id="cbdc4-133">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-133">Resource group name.</span></span>

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

### <span data-ttu-id="cbdc4-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="cbdc4-134">-SourceImage</span></span>
<span data-ttu-id="cbdc4-135">A forrás kép tárházának neve.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-135">Repository name of the source image.</span></span>

<span data-ttu-id="cbdc4-136">Adjon meg egy képet tárház szerint ("Helló-világ").</span><span class="sxs-lookup"><span data-stu-id="cbdc4-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="cbdc4-137">Ez a ' legújabb ' címkét fogja használni.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="cbdc4-138">Adjon meg egy képet a címke szerint ("Helló-világ: legújabb").</span><span class="sxs-lookup"><span data-stu-id="cbdc4-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="cbdc4-139">Adjon meg egy képet egy sha256-alapú manifest Digest (' hello-world@sha256:abc123 ') segítségével.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc4-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="cbdc4-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="cbdc4-141">A forrás Azure-tároló beállításjegyzékének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc4-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="cbdc4-142">-SourceRegistryUri</span></span>
<span data-ttu-id="cbdc4-143">A forrás beállításjegyzékének címe (például "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="cbdc4-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc4-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="cbdc4-144">-TargetTag</span></span>
<span data-ttu-id="cbdc4-145">A repo \[ : címke karakterlánca \] .</span><span class="sxs-lookup"><span data-stu-id="cbdc4-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="cbdc4-146">Ha a címke nincs kihagyva, a program a forrást fogja használni (vagy a "legújabb", ha a forrás címke is hiányzik).</span><span class="sxs-lookup"><span data-stu-id="cbdc4-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc4-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="cbdc4-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="cbdc4-148">A repositoryk neveinek listája csak a manifesztek másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="cbdc4-149">A program nem hoz létre címkét.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc4-150">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="cbdc4-150">-Username</span></span>
<span data-ttu-id="cbdc4-151">A forrás-nyilvántartóval való hitelesítéshez használt Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc4-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cbdc4-152">-Confirm</span></span>
<span data-ttu-id="cbdc4-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbdc4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbdc4-154">-WhatIf</span></span>
<span data-ttu-id="cbdc4-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbdc4-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbdc4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdc4-157">CommonParameters</span></span>
<span data-ttu-id="cbdc4-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbdc4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdc4-159">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdc4-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdc4-160">INPUTS</span></span>

### <span data-ttu-id="cbdc4-161">System. String</span><span class="sxs-lookup"><span data-stu-id="cbdc4-161">System.String</span></span>

## <span data-ttu-id="cbdc4-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdc4-162">OUTPUTS</span></span>

### <span data-ttu-id="cbdc4-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbdc4-163">System.Boolean</span></span>

## <span data-ttu-id="cbdc4-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbdc4-164">NOTES</span></span>

## <span data-ttu-id="cbdc4-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbdc4-165">RELATED LINKS</span></span>
