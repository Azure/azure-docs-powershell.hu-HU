---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 7a113bad74252778c32fc1273c9c3ca587bf1c2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667112"
---
# <span data-ttu-id="1649f-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1649f-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="1649f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1649f-102">SYNOPSIS</span></span>
<span data-ttu-id="1649f-103">Újragenerálja a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="1649f-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="1649f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1649f-104">SYNTAX</span></span>

### <span data-ttu-id="1649f-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1649f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1649f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1649f-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1649f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1649f-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1649f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1649f-108">DESCRIPTION</span></span>
<span data-ttu-id="1649f-109">A Update-AzContainerRegistryCredential parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1649f-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="1649f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1649f-110">EXAMPLES</span></span>

### <span data-ttu-id="1649f-111">1. példa: bejelentkezési hitelesítő adatok újragenerálása a tároló beállításjegyzékében</span><span class="sxs-lookup"><span data-stu-id="1649f-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="1649f-112">Ez a parancs újragenerálja a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="1649f-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="1649f-113">A \` \` hitelesítő adatok újragenerálásához engedélyezni kell a rendszergazdai hozzáférést a tároló beállításjegyzékének MyRegistry.</span><span class="sxs-lookup"><span data-stu-id="1649f-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="1649f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1649f-114">PARAMETERS</span></span>

### <span data-ttu-id="1649f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1649f-115">-DefaultProfile</span></span>
<span data-ttu-id="1649f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1649f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1649f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1649f-117">-Name</span></span>
<span data-ttu-id="1649f-118">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="1649f-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="1649f-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="1649f-119">-PasswordName</span></span>
<span data-ttu-id="1649f-120">Az újragenerálni kívánt jelszó neve.</span><span class="sxs-lookup"><span data-stu-id="1649f-120">The name of password to regenerate.</span></span>
<span data-ttu-id="1649f-121">Engedélyezett értékek: jelszó, password2.</span><span class="sxs-lookup"><span data-stu-id="1649f-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="1649f-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="1649f-122">-Registry</span></span>
<span data-ttu-id="1649f-123">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="1649f-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="1649f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1649f-124">-ResourceGroupName</span></span>
<span data-ttu-id="1649f-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1649f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1649f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1649f-126">-ResourceId</span></span>
<span data-ttu-id="1649f-127">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="1649f-127">The container registry resource id</span></span>

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

### <span data-ttu-id="1649f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1649f-128">-Confirm</span></span>
<span data-ttu-id="1649f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1649f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1649f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1649f-130">-WhatIf</span></span>
<span data-ttu-id="1649f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1649f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1649f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1649f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1649f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1649f-133">CommonParameters</span></span>
<span data-ttu-id="1649f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1649f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1649f-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1649f-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1649f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1649f-136">INPUTS</span></span>

### <span data-ttu-id="1649f-137">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1649f-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="1649f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1649f-138">System.String</span></span>

## <span data-ttu-id="1649f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1649f-139">OUTPUTS</span></span>

### <span data-ttu-id="1649f-140">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1649f-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="1649f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1649f-141">NOTES</span></span>

## <span data-ttu-id="1649f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1649f-142">RELATED LINKS</span></span>

[<span data-ttu-id="1649f-143">Új – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1649f-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="1649f-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1649f-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="1649f-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1649f-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

