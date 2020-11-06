---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 252a633112c28b1dc1e62a6004e3f67e2b6a343a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500340"
---
# <span data-ttu-id="0446f-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="0446f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0446f-102">SYNOPSIS</span></span>
<span data-ttu-id="0446f-103">Lehetővé teszi a forgalomirányítási profilok betöltését.</span><span class="sxs-lookup"><span data-stu-id="0446f-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0446f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0446f-104">SYNTAX</span></span>

### <span data-ttu-id="0446f-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="0446f-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0446f-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="0446f-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0446f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0446f-107">DESCRIPTION</span></span>
<span data-ttu-id="0446f-108">Az **enable-AzureRmTrafficManagerProfile** parancsmag az Azure Traffic Manager-profil engedélyezését teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="0446f-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0446f-109">Megadhatja a profil objektumát a csővezeték vagy a paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="0446f-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="0446f-110">Azt is megteheti, hogy a *név* és a *ResourceGroupName* paraméterrel megadhatja a profilt.</span><span class="sxs-lookup"><span data-stu-id="0446f-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="0446f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0446f-111">EXAMPLES</span></span>

### <span data-ttu-id="0446f-112">1. példa: név szerint megadott profil engedélyezése</span><span class="sxs-lookup"><span data-stu-id="0446f-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0446f-113">Ez a parancs engedélyezi a ContosoProfile nevű profilt a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="0446f-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="0446f-114">2. példa: profil engedélyezése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="0446f-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="0446f-115">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="0446f-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0446f-116">Ekkor a parancs átadja ezt a profilt az **enable-AzureRmTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="0446f-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0446f-117">Ez a parancsmag engedélyezi ezt a profilt.</span><span class="sxs-lookup"><span data-stu-id="0446f-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="0446f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0446f-118">PARAMETERS</span></span>

### <span data-ttu-id="0446f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-119">-DefaultProfile</span></span>
<span data-ttu-id="0446f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0446f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0446f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0446f-121">-Name</span></span>
<span data-ttu-id="0446f-122">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre ez a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="0446f-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0446f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0446f-123">-ResourceGroupName</span></span>
<span data-ttu-id="0446f-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0446f-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0446f-125">Ez a parancsmag lehetővé teszi a forgalomirányító profilját abban a csoportban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="0446f-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0446f-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="0446f-127">Megadja az engedélyezni kívánt **TrafficManagerProfile** objektumot.</span><span class="sxs-lookup"><span data-stu-id="0446f-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="0446f-128">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0446f-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0446f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0446f-129">CommonParameters</span></span>
<span data-ttu-id="0446f-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0446f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0446f-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0446f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0446f-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0446f-132">INPUTS</span></span>

### <span data-ttu-id="0446f-133">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0446f-134">Ez a parancsmag a **TrafficManagerProfile** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="0446f-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="0446f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0446f-135">OUTPUTS</span></span>

### <span data-ttu-id="0446f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0446f-136">System.Boolean</span></span>

## <span data-ttu-id="0446f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0446f-137">NOTES</span></span>

## <span data-ttu-id="0446f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0446f-138">RELATED LINKS</span></span>

[<span data-ttu-id="0446f-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0446f-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0446f-141">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0446f-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0446f-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0446f-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


