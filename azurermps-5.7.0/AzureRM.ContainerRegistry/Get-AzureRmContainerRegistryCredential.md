---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 68ef1cf00adeec785faf3c3f43ff2e7dbcaafbc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503807"
---
# <span data-ttu-id="7f3be-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="7f3be-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="7f3be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f3be-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3be-103">Beolvassa a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="7f3be-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f3be-104">SYNTAX</span></span>

### <span data-ttu-id="7f3be-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f3be-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f3be-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f3be-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f3be-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f3be-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f3be-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f3be-108">DESCRIPTION</span></span>
<span data-ttu-id="7f3be-109">A Get-AzureRmContainerRegistryCredential parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7f3be-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="7f3be-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7f3be-110">EXAMPLES</span></span>

### <span data-ttu-id="7f3be-111">Példa 1: bejelentkezési hitelesítő adatok beszerzése a tároló beállításjegyzékéhez</span><span class="sxs-lookup"><span data-stu-id="7f3be-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="7f3be-112">Ez a parancs a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7f3be-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="7f3be-113">A \` \` hitelesítő adatok beszerzéséhez rendszergazdai jogosultságot kell adni a rendszergazdai MyRegistry a tároló beállításjegyzékéhez.</span><span class="sxs-lookup"><span data-stu-id="7f3be-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="7f3be-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f3be-114">PARAMETERS</span></span>

### <span data-ttu-id="7f3be-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f3be-115">-Name</span></span>
<span data-ttu-id="7f3be-116">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="7f3be-116">Container Registry Name.</span></span>

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

### <span data-ttu-id="7f3be-117">-Registry</span><span class="sxs-lookup"><span data-stu-id="7f3be-117">-Registry</span></span>
<span data-ttu-id="7f3be-118">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="7f3be-118">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3be-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f3be-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7f3be-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f3be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3be-121">-DefaultProfile</span></span>
<span data-ttu-id="7f3be-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f3be-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f3be-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f3be-123">-ResourceId</span></span>
<span data-ttu-id="7f3be-124">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="7f3be-124">The container registry resource id</span></span>

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

### <span data-ttu-id="7f3be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3be-125">CommonParameters</span></span>
<span data-ttu-id="7f3be-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f3be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3be-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3be-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3be-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f3be-128">INPUTS</span></span>

### <span data-ttu-id="7f3be-129">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7f3be-129">PSContainerRegistry</span></span>
<span data-ttu-id="7f3be-130">A "Registry" paraméter elfogadja a "PSContainerRegistry" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7f3be-130">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="7f3be-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f3be-131">OUTPUTS</span></span>

### <span data-ttu-id="7f3be-132">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="7f3be-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="7f3be-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f3be-133">NOTES</span></span>

## <span data-ttu-id="7f3be-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f3be-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f3be-135">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7f3be-135">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="7f3be-136">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7f3be-136">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="7f3be-137">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="7f3be-137">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

