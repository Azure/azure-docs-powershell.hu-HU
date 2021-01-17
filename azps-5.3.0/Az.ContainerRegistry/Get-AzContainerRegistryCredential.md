---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480640"
---
# <span data-ttu-id="44f24-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="44f24-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="44f24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44f24-102">SYNOPSIS</span></span>
<span data-ttu-id="44f24-103">Egy tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44f24-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="44f24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44f24-104">SYNTAX</span></span>

### <span data-ttu-id="44f24-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44f24-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44f24-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44f24-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44f24-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44f24-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44f24-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44f24-108">DESCRIPTION</span></span>
<span data-ttu-id="44f24-109">A Get-AzContainerRegistryCredential parancsmag egy tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44f24-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="44f24-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44f24-110">EXAMPLES</span></span>

### <span data-ttu-id="44f24-111">1. példa: A tárolóadatbázishoz szükséges hitelesítő adatok lekérte</span><span class="sxs-lookup"><span data-stu-id="44f24-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="44f24-112">Ez a parancs a megadott tárolóadatbázishoz szükséges hitelesítő adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44f24-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="44f24-113">A rendszergazdai felhasználónak engedélyeznie kell a MyRegistry tárolóadatbázist \` a bejelentkezési hitelesítő adatok \` megadásához.</span><span class="sxs-lookup"><span data-stu-id="44f24-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="44f24-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44f24-114">PARAMETERS</span></span>

### <span data-ttu-id="44f24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f24-115">-DefaultProfile</span></span>
<span data-ttu-id="44f24-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="44f24-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44f24-117">-Name</span><span class="sxs-lookup"><span data-stu-id="44f24-117">-Name</span></span>
<span data-ttu-id="44f24-118">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="44f24-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f24-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="44f24-119">-Registry</span></span>
<span data-ttu-id="44f24-120">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="44f24-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f24-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f24-121">-ResourceGroupName</span></span>
<span data-ttu-id="44f24-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44f24-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f24-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44f24-123">-ResourceId</span></span>
<span data-ttu-id="44f24-124">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="44f24-124">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f24-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f24-125">CommonParameters</span></span>
<span data-ttu-id="44f24-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f24-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f24-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44f24-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f24-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44f24-128">INPUTS</span></span>

### <span data-ttu-id="44f24-129">System.String</span><span class="sxs-lookup"><span data-stu-id="44f24-129">System.String</span></span>

## <span data-ttu-id="44f24-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44f24-130">OUTPUTS</span></span>

### <span data-ttu-id="44f24-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="44f24-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="44f24-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44f24-132">NOTES</span></span>

## <span data-ttu-id="44f24-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44f24-133">RELATED LINKS</span></span>

[<span data-ttu-id="44f24-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="44f24-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="44f24-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="44f24-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="44f24-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="44f24-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

