---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346302"
---
# <span data-ttu-id="12771-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="12771-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="12771-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12771-102">SYNOPSIS</span></span>
<span data-ttu-id="12771-103">Kép importálása egy nyilvános/Azure-beállításjegyzékből egy Azure container beállításjegyzékbe.</span><span class="sxs-lookup"><span data-stu-id="12771-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="12771-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12771-104">SYNTAX</span></span>

### <span data-ttu-id="12771-105">ImportImageByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12771-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12771-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="12771-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12771-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="12771-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12771-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="12771-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12771-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12771-109">DESCRIPTION</span></span>
<span data-ttu-id="12771-110">Kép importálása egy nyilvános/Azure-beállításjegyzékből egy Azure container beállításjegyzékbe.</span><span class="sxs-lookup"><span data-stu-id="12771-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="12771-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12771-111">EXAMPLES</span></span>

### <span data-ttu-id="12771-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="12771-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="12771-113">Importálja a foglalt postaládát az ACR-be.</span><span class="sxs-lookup"><span data-stu-id="12771-113">Import busybox to ACR.</span></span> <span data-ttu-id="12771-114">Megjegyzés:</span><span class="sxs-lookup"><span data-stu-id="12771-114">Note:</span></span> 
* <span data-ttu-id="12771-115">A "library/" függvényt a forráskép előtt kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="12771-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="12771-116">"busybox:latest" => "library/busybox:latest"</span><span class="sxs-lookup"><span data-stu-id="12771-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="12771-117">Hitelesítő adatok megadása, ha a forrás beállításjegyzéke nem érhető el nyilvánosan</span><span class="sxs-lookup"><span data-stu-id="12771-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="12771-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="12771-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="12771-119">Importálja a busybox fájlt a forrás ACR-fájlból a cél ACR-be.</span><span class="sxs-lookup"><span data-stu-id="12771-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="12771-120">Megjegyzés:</span><span class="sxs-lookup"><span data-stu-id="12771-120">Note:</span></span> 
* <span data-ttu-id="12771-121">Hitelesítő adatokra van szükség, ha a forrás beállításjegyzékének rendszergazdai felhasználója le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="12771-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="12771-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12771-122">PARAMETERS</span></span>

### <span data-ttu-id="12771-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12771-123">-DefaultProfile</span></span>
<span data-ttu-id="12771-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12771-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12771-125">-Mód</span><span class="sxs-lookup"><span data-stu-id="12771-125">-Mode</span></span>
<span data-ttu-id="12771-126">Ha kényszeríti, a meglévő célcímkék felülíródnak.</span><span class="sxs-lookup"><span data-stu-id="12771-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="12771-127">A NoForce-ban a meglévő célcímkék a másolás megkezdése előtt meghiúsulnak a műveletben.</span><span class="sxs-lookup"><span data-stu-id="12771-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="12771-128">-Password</span><span class="sxs-lookup"><span data-stu-id="12771-128">-Password</span></span>
<span data-ttu-id="12771-129">A forrásadatbázissal való hitelesítéshez használt jelszó.</span><span class="sxs-lookup"><span data-stu-id="12771-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="12771-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="12771-130">-RegistryName</span></span>
<span data-ttu-id="12771-131">Cél beállításjegyzék neve.</span><span class="sxs-lookup"><span data-stu-id="12771-131">Target registry name.</span></span>

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

### <span data-ttu-id="12771-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12771-132">-ResourceGroupName</span></span>
<span data-ttu-id="12771-133">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="12771-133">Resource group name.</span></span>

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

### <span data-ttu-id="12771-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="12771-134">-SourceImage</span></span>
<span data-ttu-id="12771-135">A forráskép tárházneve.</span><span class="sxs-lookup"><span data-stu-id="12771-135">Repository name of the source image.</span></span>

<span data-ttu-id="12771-136">Adjon meg egy képet tárház ('hello-world') szerint.</span><span class="sxs-lookup"><span data-stu-id="12771-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="12771-137">Ez a "legújabb" címkét fogja használni.</span><span class="sxs-lookup"><span data-stu-id="12771-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="12771-138">Adjon meg egy képet címke szerint ('hello-world:latest').</span><span class="sxs-lookup"><span data-stu-id="12771-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="12771-139">Adjon meg egy képet sha256-alapú jegyzékfájl-kivonat (' hello-world@sha256:abc123 ') szerint.</span><span class="sxs-lookup"><span data-stu-id="12771-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="12771-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="12771-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="12771-141">A forrás Azure Container Registry erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="12771-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="12771-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="12771-142">-SourceRegistryUri</span></span>
<span data-ttu-id="12771-143">A forrás beállításjegyzékének címe (például "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="12771-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="12771-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="12771-144">-TargetTag</span></span>
<span data-ttu-id="12771-145">Az űrlap repo :tag karakterláncának \[ \] listája.</span><span class="sxs-lookup"><span data-stu-id="12771-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="12771-146">Ha nem ad meg címkét, a rendszer a forrást használja (vagy ha a forráscímke hiányzik, a "legújabb" címkét).</span><span class="sxs-lookup"><span data-stu-id="12771-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="12771-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="12771-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="12771-148">Az adattárnevek karakterláncai, amelyekből csak egy jegyzékfájlt kell másolni.</span><span class="sxs-lookup"><span data-stu-id="12771-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="12771-149">A rendszer nem hoz létre címkét.</span><span class="sxs-lookup"><span data-stu-id="12771-149">No tag will be created.</span></span>

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

### <span data-ttu-id="12771-150">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="12771-150">-Username</span></span>
<span data-ttu-id="12771-151">A forrásadatbázissal hitelesíthető felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="12771-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="12771-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12771-152">-Confirm</span></span>
<span data-ttu-id="12771-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="12771-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12771-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12771-154">-WhatIf</span></span>
<span data-ttu-id="12771-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="12771-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12771-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12771-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12771-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12771-157">CommonParameters</span></span>
<span data-ttu-id="12771-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12771-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12771-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12771-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12771-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12771-160">INPUTS</span></span>

### <span data-ttu-id="12771-161">System.String</span><span class="sxs-lookup"><span data-stu-id="12771-161">System.String</span></span>

## <span data-ttu-id="12771-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12771-162">OUTPUTS</span></span>

### <span data-ttu-id="12771-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="12771-163">System.Boolean</span></span>

## <span data-ttu-id="12771-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12771-164">NOTES</span></span>

## <span data-ttu-id="12771-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12771-165">RELATED LINKS</span></span>
