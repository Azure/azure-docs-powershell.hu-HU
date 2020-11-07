---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 89b3f47953c4074088c1ae5e2cf8e5f51ff383e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667134"
---
# <span data-ttu-id="3ec1d-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="3ec1d-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="3ec1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ec1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec1d-103">Beolvassa a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="3ec1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ec1d-104">SYNTAX</span></span>

### <span data-ttu-id="3ec1d-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ec1d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ec1d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ec1d-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ec1d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ec1d-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ec1d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ec1d-108">DESCRIPTION</span></span>
<span data-ttu-id="3ec1d-109">A Get-AzContainerRegistryCredential parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="3ec1d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ec1d-110">EXAMPLES</span></span>

### <span data-ttu-id="3ec1d-111">Példa 1: bejelentkezési hitelesítő adatok beszerzése a tároló beállításjegyzékéhez</span><span class="sxs-lookup"><span data-stu-id="3ec1d-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="3ec1d-112">Ez a parancs a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="3ec1d-113">A \` \` hitelesítő adatok beszerzéséhez rendszergazdai jogosultságot kell adni a rendszergazdai MyRegistry a tároló beállításjegyzékéhez.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="3ec1d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-114">PARAMETERS</span></span>

### <span data-ttu-id="3ec1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec1d-115">-DefaultProfile</span></span>
<span data-ttu-id="3ec1d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3ec1d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ec1d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ec1d-117">-Name</span></span>
<span data-ttu-id="3ec1d-118">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="3ec1d-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="3ec1d-119">-Registry</span></span>
<span data-ttu-id="3ec1d-120">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="3ec1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ec1d-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3ec1d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ec1d-123">-ResourceId</span></span>
<span data-ttu-id="3ec1d-124">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="3ec1d-124">The container registry resource id</span></span>

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

### <span data-ttu-id="3ec1d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec1d-125">CommonParameters</span></span>
<span data-ttu-id="3ec1d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ec1d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec1d-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec1d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-128">INPUTS</span></span>

### <span data-ttu-id="3ec1d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3ec1d-129">System.String</span></span>

## <span data-ttu-id="3ec1d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-130">OUTPUTS</span></span>

### <span data-ttu-id="3ec1d-131">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="3ec1d-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="3ec1d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ec1d-132">NOTES</span></span>

## <span data-ttu-id="3ec1d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-133">RELATED LINKS</span></span>

[<span data-ttu-id="3ec1d-134">Új – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3ec1d-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="3ec1d-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3ec1d-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="3ec1d-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="3ec1d-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

