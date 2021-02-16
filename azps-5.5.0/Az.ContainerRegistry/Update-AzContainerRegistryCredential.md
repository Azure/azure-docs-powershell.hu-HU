---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148650"
---
# <span data-ttu-id="046aa-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="046aa-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="046aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="046aa-102">SYNOPSIS</span></span>
<span data-ttu-id="046aa-103">A tároló beállításjegyzékéhez használt bejelentkezési hitelesítő adatok újragenerálásával.</span><span class="sxs-lookup"><span data-stu-id="046aa-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="046aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="046aa-104">SYNTAX</span></span>

### <span data-ttu-id="046aa-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="046aa-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="046aa-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="046aa-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046aa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="046aa-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046aa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="046aa-108">DESCRIPTION</span></span>
<span data-ttu-id="046aa-109">A Update-AzContainerRegistryCredential parancsmag újra létrehozza a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="046aa-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="046aa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="046aa-110">EXAMPLES</span></span>

### <span data-ttu-id="046aa-111">1. példa: A tárolóadatbázis hitelesítő adatainak újragenerálása</span><span class="sxs-lookup"><span data-stu-id="046aa-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="046aa-112">Ez a parancs a megadott tárolóadatbázishoz újra létrehozza a bejelentkezési hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="046aa-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="046aa-113">A rendszergazdai felhasználónak engedélyeznie kell a MyRegistry tárolóadatbázist a bejelentkezési hitelesítő adatok \` \` újragenerálásához.</span><span class="sxs-lookup"><span data-stu-id="046aa-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="046aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="046aa-114">PARAMETERS</span></span>

### <span data-ttu-id="046aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046aa-115">-DefaultProfile</span></span>
<span data-ttu-id="046aa-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="046aa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="046aa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="046aa-117">-Name</span></span>
<span data-ttu-id="046aa-118">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="046aa-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="046aa-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="046aa-119">-PasswordName</span></span>
<span data-ttu-id="046aa-120">Az újragenerálni szükséges jelszó neve.</span><span class="sxs-lookup"><span data-stu-id="046aa-120">The name of password to regenerate.</span></span>
<span data-ttu-id="046aa-121">Engedélyezett értékek: jelszó, jelszó2.</span><span class="sxs-lookup"><span data-stu-id="046aa-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="046aa-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="046aa-122">-Registry</span></span>
<span data-ttu-id="046aa-123">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="046aa-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="046aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="046aa-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="046aa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="046aa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="046aa-126">-ResourceId</span></span>
<span data-ttu-id="046aa-127">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="046aa-127">The container registry resource id</span></span>

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

### <span data-ttu-id="046aa-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="046aa-128">-Confirm</span></span>
<span data-ttu-id="046aa-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="046aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046aa-130">-WhatIf</span></span>
<span data-ttu-id="046aa-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="046aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046aa-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="046aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046aa-133">CommonParameters</span></span>
<span data-ttu-id="046aa-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046aa-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="046aa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046aa-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="046aa-136">INPUTS</span></span>

### <span data-ttu-id="046aa-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="046aa-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="046aa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="046aa-138">System.String</span></span>

## <span data-ttu-id="046aa-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="046aa-139">OUTPUTS</span></span>

### <span data-ttu-id="046aa-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="046aa-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="046aa-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="046aa-141">NOTES</span></span>

## <span data-ttu-id="046aa-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="046aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="046aa-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="046aa-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="046aa-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="046aa-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="046aa-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="046aa-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

