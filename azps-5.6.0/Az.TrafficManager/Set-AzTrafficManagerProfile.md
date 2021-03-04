---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936425"
---
# <span data-ttu-id="94130-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94130-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="94130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94130-102">SYNOPSIS</span></span>
<span data-ttu-id="94130-103">Frissíti a Forgalomkezelő-profilt.</span><span class="sxs-lookup"><span data-stu-id="94130-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="94130-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94130-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94130-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94130-105">DESCRIPTION</span></span>
<span data-ttu-id="94130-106">A **Set-AzTrafficManagerProfile parancsmag** frissíti az Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="94130-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="94130-107">Ez a parancsmag frissíti a profil beállításait egy helyi profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="94130-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="94130-108">A profilobjektumot a *TrafficManagerProfile* paraméterrel vagy a folyamat használatával adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="94130-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="94130-109">A profilt képviselő helyi objektumot a Get-AzTrafficManagerProfile használatával szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="94130-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="94130-110">Módosítsa az objektumot helyileg, majd a Módosítások véglegesítéséhez használja a **Set-AzTrafficManagerProfile-t.**</span><span class="sxs-lookup"><span data-stu-id="94130-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="94130-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94130-111">EXAMPLES</span></span>

### <span data-ttu-id="94130-112">1. példa: Profil frissítése</span><span class="sxs-lookup"><span data-stu-id="94130-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="94130-113">Az első parancs egy Azure Traffic Manager-profilt kap a Get-AzTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="94130-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="94130-114">A parancs helyileg tárolja a profilt a $TrafficManagerProfile változóban.</span><span class="sxs-lookup"><span data-stu-id="94130-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="94130-115">A második parancs helyileg módosítja a profilt.</span><span class="sxs-lookup"><span data-stu-id="94130-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="94130-116">Ez a parancs letiltja a profilt.</span><span class="sxs-lookup"><span data-stu-id="94130-116">This command disables the profile.</span></span>

<span data-ttu-id="94130-117">A harmadik parancs frissíti a ContosoProfile nevű Forgalomkezelő-profilt, hogy megfeleljen a helyi $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="94130-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="94130-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94130-118">PARAMETERS</span></span>

### <span data-ttu-id="94130-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94130-119">-DefaultProfile</span></span>
<span data-ttu-id="94130-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94130-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94130-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94130-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="94130-122">Helyi **TrafficManagerProfile objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="94130-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="94130-123">Ez a parancsmag frissíti a Traffic Managert, hogy megfeleljen ennek a helyi objektumnak.</span><span class="sxs-lookup"><span data-stu-id="94130-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94130-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94130-124">CommonParameters</span></span>
<span data-ttu-id="94130-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94130-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94130-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94130-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94130-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94130-127">INPUTS</span></span>

### <span data-ttu-id="94130-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94130-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="94130-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94130-129">OUTPUTS</span></span>

### <span data-ttu-id="94130-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94130-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="94130-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94130-131">NOTES</span></span>

## <span data-ttu-id="94130-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94130-132">RELATED LINKS</span></span>

[<span data-ttu-id="94130-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="94130-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="94130-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94130-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="94130-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94130-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="94130-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="94130-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="94130-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94130-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


