---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495139"
---
# <span data-ttu-id="3dd58-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="3dd58-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="3dd58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3dd58-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd58-103">Azure DevSpaces-vezérlő beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="3dd58-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dd58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3dd58-104">SYNTAX</span></span>

### <span data-ttu-id="3dd58-105">ListDevSpacesControllerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3dd58-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3dd58-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dd58-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dd58-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3dd58-107">DESCRIPTION</span></span>
<span data-ttu-id="3dd58-108">Azure DevSpaces-vezérlő beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="3dd58-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="3dd58-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3dd58-109">EXAMPLES</span></span>

### <span data-ttu-id="3dd58-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3dd58-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="3dd58-111">Az előfizetésben szereplő összes vezérlő listázása</span><span class="sxs-lookup"><span data-stu-id="3dd58-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="3dd58-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="3dd58-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="3dd58-113">DevSpaces-vezérlők beszerzése előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3dd58-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="3dd58-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3dd58-114">PARAMETERS</span></span>

### <span data-ttu-id="3dd58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd58-115">-DefaultProfile</span></span>
<span data-ttu-id="3dd58-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3dd58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd58-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3dd58-117">-Name</span></span>
<span data-ttu-id="3dd58-118">DevSpaces-vezérlő neve</span><span class="sxs-lookup"><span data-stu-id="3dd58-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd58-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd58-119">-ResourceGroupName</span></span>
<span data-ttu-id="3dd58-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3dd58-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd58-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd58-121">CommonParameters</span></span>
<span data-ttu-id="3dd58-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3dd58-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd58-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd58-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd58-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dd58-124">INPUTS</span></span>

### <span data-ttu-id="3dd58-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="3dd58-125">None</span></span>

## <span data-ttu-id="3dd58-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dd58-126">OUTPUTS</span></span>

### <span data-ttu-id="3dd58-127">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="3dd58-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="3dd58-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3dd58-128">NOTES</span></span>

## <span data-ttu-id="3dd58-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dd58-129">RELATED LINKS</span></span>
