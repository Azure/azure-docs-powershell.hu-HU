---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185564"
---
# <span data-ttu-id="bde1f-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="bde1f-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="bde1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bde1f-102">SYNOPSIS</span></span>
<span data-ttu-id="bde1f-103">Azure DevSpaces-vezérlő beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="bde1f-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="bde1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bde1f-104">SYNTAX</span></span>

### <span data-ttu-id="bde1f-105">ListDevSpacesControllerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bde1f-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bde1f-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bde1f-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bde1f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bde1f-107">DESCRIPTION</span></span>
<span data-ttu-id="bde1f-108">Azure DevSpaces-vezérlő beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="bde1f-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="bde1f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bde1f-109">EXAMPLES</span></span>

### <span data-ttu-id="bde1f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bde1f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="bde1f-111">Az előfizetésben szereplő összes vezérlő listázása</span><span class="sxs-lookup"><span data-stu-id="bde1f-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="bde1f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="bde1f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="bde1f-113">DevSpaces-vezérlők beszerzése előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="bde1f-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="bde1f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bde1f-114">PARAMETERS</span></span>

### <span data-ttu-id="bde1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde1f-115">-DefaultProfile</span></span>
<span data-ttu-id="bde1f-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bde1f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bde1f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bde1f-117">-Name</span></span>
<span data-ttu-id="bde1f-118">DevSpaces-vezérlő neve</span><span class="sxs-lookup"><span data-stu-id="bde1f-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="bde1f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bde1f-119">-ResourceGroupName</span></span>
<span data-ttu-id="bde1f-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="bde1f-120">Resource group name</span></span>

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

### <span data-ttu-id="bde1f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde1f-121">CommonParameters</span></span>
<span data-ttu-id="bde1f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bde1f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde1f-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde1f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde1f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bde1f-124">INPUTS</span></span>

### <span data-ttu-id="bde1f-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="bde1f-125">None</span></span>

## <span data-ttu-id="bde1f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bde1f-126">OUTPUTS</span></span>

### <span data-ttu-id="bde1f-127">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="bde1f-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="bde1f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bde1f-128">NOTES</span></span>

## <span data-ttu-id="bde1f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bde1f-129">RELATED LINKS</span></span>
