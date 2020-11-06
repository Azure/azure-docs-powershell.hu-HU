---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504451"
---
# <span data-ttu-id="77a8b-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="77a8b-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="77a8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="77a8b-103">Újragenerálja a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="77a8b-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77a8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77a8b-104">SYNTAX</span></span>

### <span data-ttu-id="77a8b-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77a8b-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77a8b-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77a8b-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a8b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77a8b-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77a8b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="77a8b-108">DESCRIPTION</span></span>
<span data-ttu-id="77a8b-109">A Update-AzureRmContainerRegistryCredential parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="77a8b-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="77a8b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="77a8b-110">EXAMPLES</span></span>

### <span data-ttu-id="77a8b-111">1. példa: bejelentkezési hitelesítő adatok újragenerálása a tároló beállításjegyzékében</span><span class="sxs-lookup"><span data-stu-id="77a8b-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="77a8b-112">Ez a parancs újragenerálja a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="77a8b-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="77a8b-113">A \` \` hitelesítő adatok újragenerálásához engedélyezni kell a rendszergazdai hozzáférést a tároló beállításjegyzékének MyRegistry.</span><span class="sxs-lookup"><span data-stu-id="77a8b-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="77a8b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77a8b-114">PARAMETERS</span></span>

### <span data-ttu-id="77a8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a8b-115">-DefaultProfile</span></span>
<span data-ttu-id="77a8b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="77a8b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77a8b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77a8b-117">-Name</span></span>
<span data-ttu-id="77a8b-118">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="77a8b-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="77a8b-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="77a8b-119">-PasswordName</span></span>
<span data-ttu-id="77a8b-120">Az újragenerálni kívánt jelszó neve.</span><span class="sxs-lookup"><span data-stu-id="77a8b-120">The name of password to regenerate.</span></span>
<span data-ttu-id="77a8b-121">Engedélyezett értékek: jelszó, password2.</span><span class="sxs-lookup"><span data-stu-id="77a8b-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="77a8b-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="77a8b-122">-Registry</span></span>
<span data-ttu-id="77a8b-123">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="77a8b-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="77a8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77a8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="77a8b-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="77a8b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="77a8b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77a8b-126">-ResourceId</span></span>
<span data-ttu-id="77a8b-127">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="77a8b-127">The container registry resource id</span></span>

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

### <span data-ttu-id="77a8b-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77a8b-128">-Confirm</span></span>
<span data-ttu-id="77a8b-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77a8b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77a8b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77a8b-130">-WhatIf</span></span>
<span data-ttu-id="77a8b-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77a8b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77a8b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77a8b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77a8b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a8b-133">CommonParameters</span></span>
<span data-ttu-id="77a8b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77a8b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a8b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77a8b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a8b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77a8b-136">INPUTS</span></span>

### <span data-ttu-id="77a8b-137">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="77a8b-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="77a8b-138">Paraméterek: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77a8b-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="77a8b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="77a8b-139">System.String</span></span>

## <span data-ttu-id="77a8b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77a8b-140">OUTPUTS</span></span>

### <span data-ttu-id="77a8b-141">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="77a8b-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="77a8b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77a8b-142">NOTES</span></span>

## <span data-ttu-id="77a8b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77a8b-143">RELATED LINKS</span></span>

[<span data-ttu-id="77a8b-144">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="77a8b-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="77a8b-145">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="77a8b-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="77a8b-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="77a8b-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

