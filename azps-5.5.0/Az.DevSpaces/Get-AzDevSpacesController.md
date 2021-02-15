---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204223"
---
# <span data-ttu-id="f3734-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="f3734-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="f3734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3734-102">SYNOPSIS</span></span>
<span data-ttu-id="f3734-103">Szerezze be vagy sorolja fel az Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="f3734-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="f3734-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3734-104">SYNTAX</span></span>

### <span data-ttu-id="f3734-105">ListDevSpacesControllerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3734-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3734-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3734-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3734-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3734-107">DESCRIPTION</span></span>
<span data-ttu-id="f3734-108">Szerezze be vagy sorolja fel az Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="f3734-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="f3734-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3734-109">EXAMPLES</span></span>

### <span data-ttu-id="f3734-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f3734-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="f3734-111">List all controllers in a subscription.</span><span class="sxs-lookup"><span data-stu-id="f3734-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="f3734-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="f3734-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="f3734-113">DevSpaces-vezérlőket is lekért egy előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="f3734-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="f3734-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3734-114">PARAMETERS</span></span>

### <span data-ttu-id="f3734-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3734-115">-DefaultProfile</span></span>
<span data-ttu-id="f3734-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3734-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3734-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f3734-117">-Name</span></span>
<span data-ttu-id="f3734-118">DevSpaces-vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="f3734-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="f3734-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3734-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3734-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f3734-120">Resource group name</span></span>

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

### <span data-ttu-id="f3734-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3734-121">CommonParameters</span></span>
<span data-ttu-id="f3734-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3734-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3734-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3734-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3734-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3734-124">INPUTS</span></span>

### <span data-ttu-id="f3734-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="f3734-125">None</span></span>

## <span data-ttu-id="f3734-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3734-126">OUTPUTS</span></span>

### <span data-ttu-id="f3734-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="f3734-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="f3734-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3734-128">NOTES</span></span>

## <span data-ttu-id="f3734-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3734-129">RELATED LINKS</span></span>
