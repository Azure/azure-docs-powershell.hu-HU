---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 46eb802b4a91aa7ee7d370ed9ca93805497f21d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497680"
---
# <span data-ttu-id="19476-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="19476-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="19476-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19476-102">SYNOPSIS</span></span>
<span data-ttu-id="19476-103">Újragenerálja a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="19476-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19476-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19476-104">SYNTAX</span></span>

### <span data-ttu-id="19476-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19476-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19476-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19476-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19476-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19476-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19476-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="19476-108">DESCRIPTION</span></span>
<span data-ttu-id="19476-109">A Update-AzureRmContainerRegistryCredential parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="19476-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="19476-110">Példák</span><span class="sxs-lookup"><span data-stu-id="19476-110">EXAMPLES</span></span>

### <span data-ttu-id="19476-111">1. példa: bejelentkezési hitelesítő adatok újragenerálása a tároló beállításjegyzékében</span><span class="sxs-lookup"><span data-stu-id="19476-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="19476-112">Ez a parancs újragenerálja a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="19476-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="19476-113">A \` \` hitelesítő adatok újragenerálásához engedélyezni kell a rendszergazdai hozzáférést a tároló beállításjegyzékének MyRegistry.</span><span class="sxs-lookup"><span data-stu-id="19476-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="19476-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19476-114">PARAMETERS</span></span>

### <span data-ttu-id="19476-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19476-115">-Name</span></span>
<span data-ttu-id="19476-116">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="19476-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19476-117">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="19476-117">-PasswordName</span></span>
<span data-ttu-id="19476-118">Az újragenerálni kívánt jelszó neve.</span><span class="sxs-lookup"><span data-stu-id="19476-118">The name of password to regenerate.</span></span>
<span data-ttu-id="19476-119">Engedélyezett értékek: jelszó, password2.</span><span class="sxs-lookup"><span data-stu-id="19476-119">Allowed values: password, password2.</span></span>

```yaml
Type: PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19476-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="19476-120">-Registry</span></span>
<span data-ttu-id="19476-121">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="19476-121">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19476-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19476-122">-ResourceGroupName</span></span>
<span data-ttu-id="19476-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="19476-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19476-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19476-124">-Confirm</span></span>
<span data-ttu-id="19476-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19476-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19476-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19476-126">-WhatIf</span></span>
<span data-ttu-id="19476-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19476-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19476-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19476-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19476-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19476-129">-DefaultProfile</span></span>
<span data-ttu-id="19476-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19476-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19476-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19476-131">-ResourceId</span></span>
<span data-ttu-id="19476-132">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="19476-132">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19476-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19476-133">CommonParameters</span></span>
<span data-ttu-id="19476-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19476-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19476-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19476-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19476-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19476-136">INPUTS</span></span>

### <span data-ttu-id="19476-137">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19476-137">PSContainerRegistry</span></span>
<span data-ttu-id="19476-138">A "Registry" paraméter elfogadja a "PSContainerRegistry" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="19476-138">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="19476-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19476-139">OUTPUTS</span></span>

### <span data-ttu-id="19476-140">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="19476-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="19476-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19476-141">NOTES</span></span>

## <span data-ttu-id="19476-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19476-142">RELATED LINKS</span></span>

[<span data-ttu-id="19476-143">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19476-143">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="19476-144">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19476-144">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="19476-145">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="19476-145">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

