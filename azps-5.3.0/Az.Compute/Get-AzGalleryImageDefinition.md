---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: c6c689ce2c9ccda71150f221bdea4ae5dd2a20fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480879"
---
# <span data-ttu-id="c4d14-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="c4d14-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="c4d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4d14-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d14-103">Get or list gallery image definitions.</span><span class="sxs-lookup"><span data-stu-id="c4d14-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="c4d14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4d14-104">SYNTAX</span></span>

### <span data-ttu-id="c4d14-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4d14-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4d14-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c4d14-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4d14-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4d14-107">DESCRIPTION</span></span>
<span data-ttu-id="c4d14-108">Get or list gallery image definitions.</span><span class="sxs-lookup"><span data-stu-id="c4d14-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="c4d14-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4d14-109">EXAMPLES</span></span>

### <span data-ttu-id="c4d14-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c4d14-110">Example 1</span></span>
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

<span data-ttu-id="c4d14-111">A gyűjtemény képdefiníciójának lekérte.</span><span class="sxs-lookup"><span data-stu-id="c4d14-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="c4d14-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c4d14-112">Example 2</span></span>
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

<span data-ttu-id="c4d14-113">Szerezze be a "kép" szótól induló képdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="c4d14-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="c4d14-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c4d14-114">Example 3</span></span>
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

<span data-ttu-id="c4d14-115">A gyűjtemény képdefiníciói a gallery1 gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="c4d14-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="c4d14-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4d14-116">PARAMETERS</span></span>

### <span data-ttu-id="c4d14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d14-117">-DefaultProfile</span></span>
<span data-ttu-id="c4d14-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4d14-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4d14-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="c4d14-119">-GalleryName</span></span>
<span data-ttu-id="c4d14-120">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c4d14-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="c4d14-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c4d14-121">-Name</span></span>
<span data-ttu-id="c4d14-122">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="c4d14-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="c4d14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d14-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4d14-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4d14-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4d14-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d14-125">-ResourceId</span></span>
<span data-ttu-id="c4d14-126">A gyűjtemény képdefiníciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c4d14-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="c4d14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d14-127">CommonParameters</span></span>
<span data-ttu-id="c4d14-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d14-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4d14-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d14-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4d14-130">INPUTS</span></span>

### <span data-ttu-id="c4d14-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c4d14-131">System.String</span></span>

## <span data-ttu-id="c4d14-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4d14-132">OUTPUTS</span></span>

### <span data-ttu-id="c4d14-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="c4d14-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="c4d14-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4d14-134">NOTES</span></span>

## <span data-ttu-id="c4d14-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4d14-135">RELATED LINKS</span></span>
