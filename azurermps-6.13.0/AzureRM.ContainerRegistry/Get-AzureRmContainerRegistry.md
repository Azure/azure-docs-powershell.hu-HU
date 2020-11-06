---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: 3d9580549308c17c92037b3e31a337f11bbe6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491976"
---
# <span data-ttu-id="51b27-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51b27-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="51b27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51b27-102">SYNOPSIS</span></span>
<span data-ttu-id="51b27-103">Tároló-nyilvántartót kap.</span><span class="sxs-lookup"><span data-stu-id="51b27-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51b27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51b27-104">SYNTAX</span></span>

### <span data-ttu-id="51b27-105">ListRegistriesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51b27-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b27-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51b27-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b27-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51b27-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51b27-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="51b27-108">DESCRIPTION</span></span>
<span data-ttu-id="51b27-109">A Get-AzureRmContainerRegistry parancsmag egy adott tároló rendszerleíró adatbázisát vagy egy erőforráscsoport összes tároló-nyilvántartását, illetve az előfizetést kapja meg.</span><span class="sxs-lookup"><span data-stu-id="51b27-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="51b27-110">Példák</span><span class="sxs-lookup"><span data-stu-id="51b27-110">EXAMPLES</span></span>

### <span data-ttu-id="51b27-111">1. példa: a megadott tároló beállításjegyzékének beszerzése</span><span class="sxs-lookup"><span data-stu-id="51b27-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="51b27-112">Ez a parancs a megadott tároló beállításjegyzékét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="51b27-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="51b27-113">2. példa: egy erőforráscsoport összes tároló-nyilvántartásának lekérése</span><span class="sxs-lookup"><span data-stu-id="51b27-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="51b27-114">Ez a parancs egy erőforráscsoport minden tároló-nyilvántartását beolvassa.</span><span class="sxs-lookup"><span data-stu-id="51b27-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="51b27-115">3. példa: az előfizetésben szereplő összes tároló-nyilvántartó-bejegyzés beszerzése</span><span class="sxs-lookup"><span data-stu-id="51b27-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="51b27-116">Ez a parancs beilleszti az előfizetéshez tartozó összes tároló-nyilvántartót.</span><span class="sxs-lookup"><span data-stu-id="51b27-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="51b27-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51b27-117">PARAMETERS</span></span>

### <span data-ttu-id="51b27-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b27-118">-DefaultProfile</span></span>
<span data-ttu-id="51b27-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="51b27-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51b27-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="51b27-120">-IncludeDetail</span></span>
<span data-ttu-id="51b27-121">További részletek megjelenítése a tároló beállításjegyzékéről.</span><span class="sxs-lookup"><span data-stu-id="51b27-121">Show more details about the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b27-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51b27-122">-Name</span></span>
<span data-ttu-id="51b27-123">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="51b27-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b27-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b27-124">-ResourceGroupName</span></span>
<span data-ttu-id="51b27-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="51b27-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b27-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b27-126">-ResourceId</span></span>
<span data-ttu-id="51b27-127">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="51b27-127">The container registry resource id</span></span>

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

### <span data-ttu-id="51b27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b27-128">CommonParameters</span></span>
<span data-ttu-id="51b27-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51b27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b27-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b27-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b27-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51b27-131">INPUTS</span></span>

### <span data-ttu-id="51b27-132">System. String</span><span class="sxs-lookup"><span data-stu-id="51b27-132">System.String</span></span>

## <span data-ttu-id="51b27-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51b27-133">OUTPUTS</span></span>

### <span data-ttu-id="51b27-134">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51b27-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="51b27-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51b27-135">NOTES</span></span>

## <span data-ttu-id="51b27-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51b27-136">RELATED LINKS</span></span>

[<span data-ttu-id="51b27-137">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51b27-137">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="51b27-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51b27-138">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="51b27-139">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51b27-139">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

