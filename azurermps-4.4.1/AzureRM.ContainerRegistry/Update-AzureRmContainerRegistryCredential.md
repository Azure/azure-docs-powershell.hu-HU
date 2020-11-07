---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672707"
---
# <span data-ttu-id="c9b2f-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c9b2f-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="c9b2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b2f-103">Újragenerálja a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9b2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9b2f-104">SYNTAX</span></span>

### <span data-ttu-id="c9b2f-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9b2f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9b2f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b2f-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9b2f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9b2f-107">DESCRIPTION</span></span>
<span data-ttu-id="c9b2f-108">Az **Update-AzureRmContainerRegistryCredential** parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="c9b2f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c9b2f-109">EXAMPLES</span></span>

### <span data-ttu-id="c9b2f-110">1. példa: bejelentkezési hitelesítő adatok újragenerálása a tároló beállításjegyzékében</span><span class="sxs-lookup"><span data-stu-id="c9b2f-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="c9b2f-111">Ez a parancs újragenerálja a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="c9b2f-112">A hitelesítő adatok újragenerálásához engedélyezni kell a rendszergazdai hozzáférést a tároló beállításjegyzékéhez `MyRegistry` .</span><span class="sxs-lookup"><span data-stu-id="c9b2f-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="c9b2f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9b2f-113">PARAMETERS</span></span>

### <span data-ttu-id="c9b2f-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9b2f-114">-Name</span></span>
<span data-ttu-id="c9b2f-115">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="c9b2f-116">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="c9b2f-116">-PasswordName</span></span>
<span data-ttu-id="c9b2f-117">Az újragenerálni kívánt jelszó neve.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-117">The name of password to regenerate.</span></span>
<span data-ttu-id="c9b2f-118">Engedélyezett értékek: jelszó, password2.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b2f-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="c9b2f-119">-Registry</span></span>
<span data-ttu-id="c9b2f-120">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="c9b2f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b2f-121">-ResourceGroupName</span></span>
<span data-ttu-id="c9b2f-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c9b2f-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9b2f-123">-Confirm</span></span>
<span data-ttu-id="c9b2f-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b2f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b2f-125">-WhatIf</span></span>
<span data-ttu-id="c9b2f-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b2f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b2f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b2f-128">-DefaultProfile</span></span>
<span data-ttu-id="c9b2f-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9b2f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b2f-130">CommonParameters</span></span>
<span data-ttu-id="c9b2f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9b2f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b2f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b2f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b2f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9b2f-133">INPUTS</span></span>

### <span data-ttu-id="c9b2f-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c9b2f-134">PSContainerRegistry</span></span>
<span data-ttu-id="c9b2f-135">A "Registry" paraméter elfogadja a "PSContainerRegistry" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c9b2f-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="c9b2f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9b2f-136">OUTPUTS</span></span>

### <span data-ttu-id="c9b2f-137">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c9b2f-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="c9b2f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9b2f-138">NOTES</span></span>

## <span data-ttu-id="c9b2f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9b2f-139">RELATED LINKS</span></span>

[<span data-ttu-id="c9b2f-140">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c9b2f-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="c9b2f-141">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c9b2f-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="c9b2f-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c9b2f-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

