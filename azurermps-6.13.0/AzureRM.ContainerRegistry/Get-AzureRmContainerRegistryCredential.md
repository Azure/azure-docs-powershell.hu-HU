---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491975"
---
# <span data-ttu-id="fa88f-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fa88f-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="fa88f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa88f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa88f-103">Beolvassa a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="fa88f-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa88f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa88f-104">SYNTAX</span></span>

### <span data-ttu-id="fa88f-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa88f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa88f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa88f-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa88f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa88f-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa88f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa88f-108">DESCRIPTION</span></span>
<span data-ttu-id="fa88f-109">A Get-AzureRmContainerRegistryCredential parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fa88f-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="fa88f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fa88f-110">EXAMPLES</span></span>

### <span data-ttu-id="fa88f-111">Példa 1: bejelentkezési hitelesítő adatok beszerzése a tároló beállításjegyzékéhez</span><span class="sxs-lookup"><span data-stu-id="fa88f-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="fa88f-112">Ez a parancs a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fa88f-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="fa88f-113">A \` \` hitelesítő adatok beszerzéséhez rendszergazdai jogosultságot kell adni a rendszergazdai MyRegistry a tároló beállításjegyzékéhez.</span><span class="sxs-lookup"><span data-stu-id="fa88f-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="fa88f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa88f-114">PARAMETERS</span></span>

### <span data-ttu-id="fa88f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa88f-115">-DefaultProfile</span></span>
<span data-ttu-id="fa88f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fa88f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa88f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa88f-117">-Name</span></span>
<span data-ttu-id="fa88f-118">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="fa88f-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="fa88f-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="fa88f-119">-Registry</span></span>
<span data-ttu-id="fa88f-120">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="fa88f-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="fa88f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa88f-121">-ResourceGroupName</span></span>
<span data-ttu-id="fa88f-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fa88f-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="fa88f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa88f-123">-ResourceId</span></span>
<span data-ttu-id="fa88f-124">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="fa88f-124">The container registry resource id</span></span>

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

### <span data-ttu-id="fa88f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa88f-125">CommonParameters</span></span>
<span data-ttu-id="fa88f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa88f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa88f-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa88f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa88f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa88f-128">INPUTS</span></span>

### <span data-ttu-id="fa88f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fa88f-129">System.String</span></span>

## <span data-ttu-id="fa88f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa88f-130">OUTPUTS</span></span>

### <span data-ttu-id="fa88f-131">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fa88f-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="fa88f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa88f-132">NOTES</span></span>

## <span data-ttu-id="fa88f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa88f-133">RELATED LINKS</span></span>

[<span data-ttu-id="fa88f-134">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fa88f-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="fa88f-135">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fa88f-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="fa88f-136">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fa88f-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

