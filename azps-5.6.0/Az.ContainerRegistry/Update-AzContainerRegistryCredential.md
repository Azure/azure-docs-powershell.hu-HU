---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 71eb25c99197513bead7cb400b8a5648c137442d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920769"
---
# <span data-ttu-id="e29d5-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e29d5-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="e29d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e29d5-103">A tároló beállításjegyzékéhez használt bejelentkezési hitelesítő adatok újragenerálásával.</span><span class="sxs-lookup"><span data-stu-id="e29d5-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="e29d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e29d5-104">SYNTAX</span></span>

### <span data-ttu-id="e29d5-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e29d5-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e29d5-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e29d5-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29d5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e29d5-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29d5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e29d5-108">DESCRIPTION</span></span>
<span data-ttu-id="e29d5-109">A Update-AzContainerRegistryCredential parancsmag újra létrehozza a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="e29d5-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="e29d5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e29d5-110">EXAMPLES</span></span>

### <span data-ttu-id="e29d5-111">1. példa: A tárolóadatbázis hitelesítő adatainak újragenerálása</span><span class="sxs-lookup"><span data-stu-id="e29d5-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="e29d5-112">Ez a parancs a megadott tárolóadatbázishoz újra létrehozza a bejelentkezési hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="e29d5-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="e29d5-113">A rendszergazdai felhasználónak engedélyeznie kell a MyRegistry tárolóadatbázist a bejelentkezési hitelesítő adatok \` \` újragenerálásához.</span><span class="sxs-lookup"><span data-stu-id="e29d5-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="e29d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e29d5-114">PARAMETERS</span></span>

### <span data-ttu-id="e29d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29d5-115">-DefaultProfile</span></span>
<span data-ttu-id="e29d5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e29d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e29d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e29d5-117">-Name</span></span>
<span data-ttu-id="e29d5-118">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="e29d5-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="e29d5-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="e29d5-119">-PasswordName</span></span>
<span data-ttu-id="e29d5-120">Az újragenerálni szükséges jelszó neve.</span><span class="sxs-lookup"><span data-stu-id="e29d5-120">The name of password to regenerate.</span></span>
<span data-ttu-id="e29d5-121">Engedélyezett értékek: jelszó, jelszó2.</span><span class="sxs-lookup"><span data-stu-id="e29d5-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29d5-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="e29d5-122">-Registry</span></span>
<span data-ttu-id="e29d5-123">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="e29d5-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e29d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="e29d5-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e29d5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e29d5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e29d5-126">-ResourceId</span></span>
<span data-ttu-id="e29d5-127">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e29d5-127">The container registry resource id</span></span>

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

### <span data-ttu-id="e29d5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e29d5-128">-Confirm</span></span>
<span data-ttu-id="e29d5-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e29d5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29d5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29d5-130">-WhatIf</span></span>
<span data-ttu-id="e29d5-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e29d5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29d5-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e29d5-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29d5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29d5-133">CommonParameters</span></span>
<span data-ttu-id="e29d5-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29d5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29d5-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e29d5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29d5-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e29d5-136">INPUTS</span></span>

### <span data-ttu-id="e29d5-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e29d5-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="e29d5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e29d5-138">System.String</span></span>

## <span data-ttu-id="e29d5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e29d5-139">OUTPUTS</span></span>

### <span data-ttu-id="e29d5-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e29d5-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="e29d5-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e29d5-141">NOTES</span></span>

## <span data-ttu-id="e29d5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e29d5-142">RELATED LINKS</span></span>

[<span data-ttu-id="e29d5-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e29d5-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="e29d5-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e29d5-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="e29d5-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e29d5-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

