---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: f7ac75789e4020d3d0e645e5dac8ef2430795eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498124"
---
# <span data-ttu-id="28b13-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="28b13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28b13-102">SYNOPSIS</span></span>
<span data-ttu-id="28b13-103">Lehetővé teszi a forgalomirányítási profilok betöltését.</span><span class="sxs-lookup"><span data-stu-id="28b13-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28b13-104">SYNTAX</span></span>

### <span data-ttu-id="28b13-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="28b13-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28b13-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="28b13-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28b13-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="28b13-107">DESCRIPTION</span></span>
<span data-ttu-id="28b13-108">Az **enable-AzureRmTrafficManagerProfile** parancsmag az Azure Traffic Manager-profil engedélyezését teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="28b13-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="28b13-109">Megadhatja a profil objektumát a csővezeték vagy a paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="28b13-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="28b13-110">Azt is megteheti, hogy a *név* és a *ResourceGroupName* paraméterrel megadhatja a profilt.</span><span class="sxs-lookup"><span data-stu-id="28b13-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="28b13-111">Példák</span><span class="sxs-lookup"><span data-stu-id="28b13-111">EXAMPLES</span></span>

### <span data-ttu-id="28b13-112">1. példa: név szerint megadott profil engedélyezése</span><span class="sxs-lookup"><span data-stu-id="28b13-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="28b13-113">Ez a parancs engedélyezi a ContosoProfile nevű profilt a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="28b13-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="28b13-114">2. példa: profil engedélyezése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="28b13-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="28b13-115">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="28b13-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="28b13-116">Ekkor a parancs átadja ezt a profilt az **enable-AzureRmTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="28b13-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="28b13-117">Ez a parancsmag engedélyezi ezt a profilt.</span><span class="sxs-lookup"><span data-stu-id="28b13-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="28b13-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28b13-118">PARAMETERS</span></span>

### <span data-ttu-id="28b13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-119">-DefaultProfile</span></span>
<span data-ttu-id="28b13-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28b13-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28b13-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28b13-121">-Name</span></span>
<span data-ttu-id="28b13-122">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre ez a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="28b13-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b13-123">-ResourceGroupName</span></span>
<span data-ttu-id="28b13-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28b13-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="28b13-125">Ez a parancsmag lehetővé teszi a forgalomirányító profilját abban a csoportban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="28b13-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b13-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="28b13-127">Megadja az engedélyezni kívánt **TrafficManagerProfile** objektumot.</span><span class="sxs-lookup"><span data-stu-id="28b13-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="28b13-128">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="28b13-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28b13-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b13-129">CommonParameters</span></span>
<span data-ttu-id="28b13-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28b13-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b13-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b13-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b13-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28b13-132">INPUTS</span></span>

### <span data-ttu-id="28b13-133">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="28b13-134">Ez a parancsmag a **TrafficManagerProfile** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="28b13-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="28b13-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28b13-135">OUTPUTS</span></span>

### <span data-ttu-id="28b13-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28b13-136">System.Boolean</span></span>

## <span data-ttu-id="28b13-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28b13-137">NOTES</span></span>

## <span data-ttu-id="28b13-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28b13-138">RELATED LINKS</span></span>

[<span data-ttu-id="28b13-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="28b13-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="28b13-141">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="28b13-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="28b13-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="28b13-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


