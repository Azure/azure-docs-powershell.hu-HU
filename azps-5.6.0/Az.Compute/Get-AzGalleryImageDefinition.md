---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: 0599226e4b9856378804aca7bce013b03456b1ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927250"
---
# <span data-ttu-id="94d84-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="94d84-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="94d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d84-102">SYNOPSIS</span></span>
<span data-ttu-id="94d84-103">Get or list gallery image definitions.</span><span class="sxs-lookup"><span data-stu-id="94d84-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="94d84-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94d84-104">SYNTAX</span></span>

### <span data-ttu-id="94d84-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94d84-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94d84-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="94d84-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94d84-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94d84-107">DESCRIPTION</span></span>
<span data-ttu-id="94d84-108">Get or list gallery image definitions.</span><span class="sxs-lookup"><span data-stu-id="94d84-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="94d84-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94d84-109">EXAMPLES</span></span>

### <span data-ttu-id="94d84-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="94d84-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="94d84-111">A gyűjtemény képdefiníciójának lekérte.</span><span class="sxs-lookup"><span data-stu-id="94d84-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="94d84-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="94d84-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="94d84-113">Szerezze be a "kép" szótól induló képdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="94d84-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="94d84-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="94d84-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="94d84-115">A gyűjtemény képdefiníciói a gallery1 gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="94d84-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="94d84-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94d84-116">PARAMETERS</span></span>

### <span data-ttu-id="94d84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d84-117">-DefaultProfile</span></span>
<span data-ttu-id="94d84-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94d84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94d84-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="94d84-119">-GalleryName</span></span>
<span data-ttu-id="94d84-120">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="94d84-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d84-121">-Name</span><span class="sxs-lookup"><span data-stu-id="94d84-121">-Name</span></span>
<span data-ttu-id="94d84-122">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="94d84-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="94d84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d84-123">-ResourceGroupName</span></span>
<span data-ttu-id="94d84-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94d84-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d84-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94d84-125">-ResourceId</span></span>
<span data-ttu-id="94d84-126">A gyűjtemény képdefiníciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="94d84-126">The resource ID for the gallery image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d84-127">CommonParameters</span></span>
<span data-ttu-id="94d84-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d84-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94d84-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d84-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94d84-130">INPUTS</span></span>

### <span data-ttu-id="94d84-131">System.String</span><span class="sxs-lookup"><span data-stu-id="94d84-131">System.String</span></span>

## <span data-ttu-id="94d84-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94d84-132">OUTPUTS</span></span>

### <span data-ttu-id="94d84-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="94d84-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="94d84-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94d84-134">NOTES</span></span>

## <span data-ttu-id="94d84-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94d84-135">RELATED LINKS</span></span>
