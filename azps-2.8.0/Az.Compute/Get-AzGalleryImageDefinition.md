---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: 86da7a6f991bf7eeead14ad3414f9210eb7e175d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667476"
---
# <span data-ttu-id="c7c62-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="c7c62-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="c7c62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7c62-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c62-103">Képdefiníciók beolvasása vagy listázása</span><span class="sxs-lookup"><span data-stu-id="c7c62-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="c7c62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7c62-104">SYNTAX</span></span>

### <span data-ttu-id="c7c62-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7c62-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7c62-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c7c62-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7c62-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7c62-107">DESCRIPTION</span></span>
<span data-ttu-id="c7c62-108">Képdefiníciók beolvasása vagy listázása</span><span class="sxs-lookup"><span data-stu-id="c7c62-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="c7c62-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c7c62-109">EXAMPLES</span></span>

### <span data-ttu-id="c7c62-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c7c62-110">Example 1</span></span>
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

<span data-ttu-id="c7c62-111">A gyűjtemény képének definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c7c62-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="c7c62-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c7c62-112">Example 2</span></span>
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

<span data-ttu-id="c7c62-113">A "kép" kezdetű gyűjtemény képének definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c7c62-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="c7c62-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c7c62-114">Example 3</span></span>
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

<span data-ttu-id="c7c62-115">Beolvashatja a gyűjtemény képdefinícióit a gallery1.</span><span class="sxs-lookup"><span data-stu-id="c7c62-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="c7c62-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7c62-116">PARAMETERS</span></span>

### <span data-ttu-id="c7c62-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c62-117">-DefaultProfile</span></span>
<span data-ttu-id="c7c62-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7c62-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c62-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="c7c62-119">-GalleryName</span></span>
<span data-ttu-id="c7c62-120">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c7c62-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="c7c62-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7c62-121">-Name</span></span>
<span data-ttu-id="c7c62-122">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="c7c62-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="c7c62-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c62-123">-ResourceGroupName</span></span>
<span data-ttu-id="c7c62-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7c62-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c7c62-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7c62-125">-ResourceId</span></span>
<span data-ttu-id="c7c62-126">A tár képdefiníciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c7c62-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="c7c62-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c62-127">CommonParameters</span></span>
<span data-ttu-id="c7c62-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7c62-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c62-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c7c62-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c62-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7c62-130">INPUTS</span></span>

### <span data-ttu-id="c7c62-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c7c62-131">System.String</span></span>

## <span data-ttu-id="c7c62-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7c62-132">OUTPUTS</span></span>

### <span data-ttu-id="c7c62-133">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="c7c62-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="c7c62-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7c62-134">NOTES</span></span>

## <span data-ttu-id="c7c62-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7c62-135">RELATED LINKS</span></span>
