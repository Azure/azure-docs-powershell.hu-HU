---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 9536e6250f73270c7700a14406cb24b8e8f31189
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492673"
---
# <span data-ttu-id="0ceb5-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="0ceb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ceb5-102">SYNOPSIS</span></span>
<span data-ttu-id="0ceb5-103">A Traffic Manager-profil frissítése</span><span class="sxs-lookup"><span data-stu-id="0ceb5-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ceb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ceb5-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ceb5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ceb5-105">DESCRIPTION</span></span>
<span data-ttu-id="0ceb5-106">A **set-AzureRmTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt frissít.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0ceb5-107">Ez a parancsmag frissíti a profil beállításait egy helyi profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="0ceb5-108">Megadhatja a profil objektumát a *TrafficManagerProfile* paraméterrel vagy a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="0ceb5-109">A Get-AzureRmTrafficManagerProfile parancsmag segítségével olyan helyi objektumot kaphat, amely egy profilt képvisel.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="0ceb5-110">Módosítsa az objektumot helyileg, majd használja a **set-AzureRmTrafficManagerProfile** a módosítások véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="0ceb5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0ceb5-111">EXAMPLES</span></span>

### <span data-ttu-id="0ceb5-112">Példa 1: profil frissítése</span><span class="sxs-lookup"><span data-stu-id="0ceb5-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="0ceb5-113">Az első parancs az Azure Traffic Manager-profilt az Get-AzureRmTrafficManagerProfile parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="0ceb5-114">A parancs a $TrafficManagerProfile változóban helyileg tárolja a profilt.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="0ceb5-115">A második parancs helyileg módosítja a profilt.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="0ceb5-116">Ez a parancs letiltja a profilt.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-116">This command disables the profile.</span></span>

<span data-ttu-id="0ceb5-117">A harmadik parancs frissíti a ContosoProfile nevű forgalomirányítási profilt az $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="0ceb5-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ceb5-118">PARAMETERS</span></span>

### <span data-ttu-id="0ceb5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-119">-DefaultProfile</span></span>
<span data-ttu-id="0ceb5-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ceb5-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="0ceb5-122">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0ceb5-123">Ez a parancsmag frissíti a Traffic Manager alkalmazást a helyi objektum egyeztetéséhez.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="0ceb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ceb5-124">CommonParameters</span></span>
<span data-ttu-id="0ceb5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ceb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ceb5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ceb5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ceb5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ceb5-127">INPUTS</span></span>

### <span data-ttu-id="0ceb5-128">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0ceb5-129">Ez a parancsmag a **TrafficManagerProfile** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="0ceb5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ceb5-130">OUTPUTS</span></span>

### <span data-ttu-id="0ceb5-131">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0ceb5-132">Ez a parancsmag egy **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="0ceb5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ceb5-133">NOTES</span></span>

## <span data-ttu-id="0ceb5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ceb5-134">RELATED LINKS</span></span>

[<span data-ttu-id="0ceb5-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0ceb5-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="0ceb5-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0ceb5-137">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0ceb5-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0ceb5-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="0ceb5-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


