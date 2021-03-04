---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: dd7ba99632cfef493fe3202b2402a938b11fa807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922994"
---
# <span data-ttu-id="31ab9-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="31ab9-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="31ab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="31ab9-103">Szerezze be vagy sorolja fel az Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="31ab9-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="31ab9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31ab9-104">SYNTAX</span></span>

### <span data-ttu-id="31ab9-105">ListDevSpacesControllerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31ab9-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31ab9-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31ab9-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31ab9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31ab9-107">DESCRIPTION</span></span>
<span data-ttu-id="31ab9-108">Szerezze be vagy sorolja fel az Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="31ab9-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="31ab9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31ab9-109">EXAMPLES</span></span>

### <span data-ttu-id="31ab9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="31ab9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="31ab9-111">List all controllers in a subscription.</span><span class="sxs-lookup"><span data-stu-id="31ab9-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="31ab9-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="31ab9-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="31ab9-113">DevSpaces-vezérlőket is lekért egy előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="31ab9-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="31ab9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31ab9-114">PARAMETERS</span></span>

### <span data-ttu-id="31ab9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ab9-115">-DefaultProfile</span></span>
<span data-ttu-id="31ab9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31ab9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31ab9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="31ab9-117">-Name</span></span>
<span data-ttu-id="31ab9-118">DevSpaces-vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="31ab9-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="31ab9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ab9-119">-ResourceGroupName</span></span>
<span data-ttu-id="31ab9-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="31ab9-120">Resource group name</span></span>

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

### <span data-ttu-id="31ab9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ab9-121">CommonParameters</span></span>
<span data-ttu-id="31ab9-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ab9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ab9-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ab9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ab9-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31ab9-124">INPUTS</span></span>

### <span data-ttu-id="31ab9-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="31ab9-125">None</span></span>

## <span data-ttu-id="31ab9-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31ab9-126">OUTPUTS</span></span>

### <span data-ttu-id="31ab9-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="31ab9-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="31ab9-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31ab9-128">NOTES</span></span>

## <span data-ttu-id="31ab9-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31ab9-129">RELATED LINKS</span></span>
