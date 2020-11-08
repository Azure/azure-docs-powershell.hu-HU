---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183442"
---
# <span data-ttu-id="f2eaa-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2eaa-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="f2eaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="f2eaa-103">A Traffic Manager-profil frissítése</span><span class="sxs-lookup"><span data-stu-id="f2eaa-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="f2eaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2eaa-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2eaa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="f2eaa-106">A **set-AzTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt frissít.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f2eaa-107">Ez a parancsmag frissíti a profil beállításait egy helyi profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="f2eaa-108">Megadhatja a profil objektumát a *TrafficManagerProfile* paraméterrel vagy a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="f2eaa-109">A Get-AzTrafficManagerProfile parancsmag segítségével olyan helyi objektumot kaphat, amely egy profilt képvisel.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f2eaa-110">Módosítsa az objektumot helyileg, majd használja a **set-AzTrafficManagerProfile** a módosítások véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="f2eaa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f2eaa-111">EXAMPLES</span></span>

### <span data-ttu-id="f2eaa-112">Példa 1: profil frissítése</span><span class="sxs-lookup"><span data-stu-id="f2eaa-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f2eaa-113">Az első parancs az Azure Traffic Manager-profilt az Get-AzTrafficManagerProfile parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f2eaa-114">A parancs a $TrafficManagerProfile változóban helyileg tárolja a profilt.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f2eaa-115">A második parancs helyileg módosítja a profilt.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="f2eaa-116">Ez a parancs letiltja a profilt.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-116">This command disables the profile.</span></span>

<span data-ttu-id="f2eaa-117">A harmadik parancs frissíti a ContosoProfile nevű forgalomirányítási profilt az $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f2eaa-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2eaa-118">PARAMETERS</span></span>

### <span data-ttu-id="f2eaa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2eaa-119">-DefaultProfile</span></span>
<span data-ttu-id="f2eaa-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2eaa-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2eaa-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="f2eaa-122">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f2eaa-123">Ez a parancsmag frissíti a Traffic Manager alkalmazást a helyi objektum egyeztetéséhez.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="f2eaa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2eaa-124">CommonParameters</span></span>
<span data-ttu-id="f2eaa-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2eaa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2eaa-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2eaa-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2eaa-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2eaa-127">INPUTS</span></span>

### <span data-ttu-id="f2eaa-128">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2eaa-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f2eaa-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2eaa-129">OUTPUTS</span></span>

### <span data-ttu-id="f2eaa-130">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2eaa-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f2eaa-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2eaa-131">NOTES</span></span>

## <span data-ttu-id="f2eaa-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2eaa-132">RELATED LINKS</span></span>

[<span data-ttu-id="f2eaa-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f2eaa-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f2eaa-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2eaa-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f2eaa-135">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2eaa-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="f2eaa-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f2eaa-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f2eaa-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2eaa-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


