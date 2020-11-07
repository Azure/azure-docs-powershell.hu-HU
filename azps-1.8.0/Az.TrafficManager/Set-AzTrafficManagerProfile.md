---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: d8f4b5e069ef273dedc8e2e5a1f929d1649aefdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668381"
---
# <span data-ttu-id="c73cb-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="c73cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c73cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c73cb-103">A Traffic Manager-profil frissítése</span><span class="sxs-lookup"><span data-stu-id="c73cb-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="c73cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c73cb-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c73cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c73cb-105">DESCRIPTION</span></span>
<span data-ttu-id="c73cb-106">A **set-AzTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt frissít.</span><span class="sxs-lookup"><span data-stu-id="c73cb-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c73cb-107">Ez a parancsmag frissíti a profil beállításait egy helyi profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="c73cb-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="c73cb-108">Megadhatja a profil objektumát a *TrafficManagerProfile* paraméterrel vagy a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="c73cb-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="c73cb-109">A Get-AzTrafficManagerProfile parancsmag segítségével olyan helyi objektumot kaphat, amely egy profilt képvisel.</span><span class="sxs-lookup"><span data-stu-id="c73cb-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="c73cb-110">Módosítsa az objektumot helyileg, majd használja a **set-AzTrafficManagerProfile** a módosítások véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="c73cb-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="c73cb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c73cb-111">EXAMPLES</span></span>

### <span data-ttu-id="c73cb-112">Példa 1: profil frissítése</span><span class="sxs-lookup"><span data-stu-id="c73cb-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="c73cb-113">Az első parancs az Azure Traffic Manager-profilt az Get-AzTrafficManagerProfile parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="c73cb-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="c73cb-114">A parancs a $TrafficManagerProfile változóban helyileg tárolja a profilt.</span><span class="sxs-lookup"><span data-stu-id="c73cb-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="c73cb-115">A második parancs helyileg módosítja a profilt.</span><span class="sxs-lookup"><span data-stu-id="c73cb-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="c73cb-116">Ez a parancs letiltja a profilt.</span><span class="sxs-lookup"><span data-stu-id="c73cb-116">This command disables the profile.</span></span>

<span data-ttu-id="c73cb-117">A harmadik parancs frissíti a ContosoProfile nevű forgalomirányítási profilt az $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="c73cb-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="c73cb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c73cb-118">PARAMETERS</span></span>

### <span data-ttu-id="c73cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-119">-DefaultProfile</span></span>
<span data-ttu-id="c73cb-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c73cb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c73cb-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="c73cb-122">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c73cb-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="c73cb-123">Ez a parancsmag frissíti a Traffic Manager alkalmazást a helyi objektum egyeztetéséhez.</span><span class="sxs-lookup"><span data-stu-id="c73cb-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="c73cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73cb-124">CommonParameters</span></span>
<span data-ttu-id="c73cb-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c73cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73cb-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c73cb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73cb-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c73cb-127">INPUTS</span></span>

### <span data-ttu-id="c73cb-128">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c73cb-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c73cb-129">OUTPUTS</span></span>

### <span data-ttu-id="c73cb-130">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c73cb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c73cb-131">NOTES</span></span>

## <span data-ttu-id="c73cb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c73cb-132">RELATED LINKS</span></span>

[<span data-ttu-id="c73cb-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c73cb-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="c73cb-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c73cb-135">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c73cb-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c73cb-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="c73cb-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


