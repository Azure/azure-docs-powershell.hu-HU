---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bdfe37622db49c554f128714ab2af65a11fbfce7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500343"
---
# <span data-ttu-id="72909-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72909-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="72909-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72909-102">SYNOPSIS</span></span>
<span data-ttu-id="72909-103">Beolvassa a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="72909-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72909-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72909-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72909-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72909-105">DESCRIPTION</span></span>
<span data-ttu-id="72909-106">A **Get-AzureRmTrafficManagerProfile** parancsmag Azure Traffic Manager-profilt kap, és egy olyan objektumot ad eredményül, amely a profilt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="72909-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="72909-107">Adjon meg egy profilt a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="72909-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="72909-108">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzureRmTrafficManagerProfile parancsmag használatával alkalmazhatja a profil módosításait.</span><span class="sxs-lookup"><span data-stu-id="72909-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="72909-109">Példák</span><span class="sxs-lookup"><span data-stu-id="72909-109">EXAMPLES</span></span>

### <span data-ttu-id="72909-110">Példa 1: profil beszerzése</span><span class="sxs-lookup"><span data-stu-id="72909-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="72909-111">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="72909-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="72909-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72909-112">PARAMETERS</span></span>

### <span data-ttu-id="72909-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72909-113">-DefaultProfile</span></span>
<span data-ttu-id="72909-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72909-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72909-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72909-115">-Name</span></span>
<span data-ttu-id="72909-116">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="72909-116">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72909-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72909-117">-ResourceGroupName</span></span>
<span data-ttu-id="72909-118">Annak a adatcsoportnak a neve, amely a parancsmag által beolvasott adatforgalmi vezető profilt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="72909-118">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72909-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72909-119">CommonParameters</span></span>
<span data-ttu-id="72909-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72909-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72909-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72909-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72909-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72909-122">INPUTS</span></span>

### <span data-ttu-id="72909-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="72909-123">None</span></span>
<span data-ttu-id="72909-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="72909-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72909-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72909-125">OUTPUTS</span></span>

### <span data-ttu-id="72909-126">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72909-126">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="72909-127">Ez a parancsmag egy **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="72909-127">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="72909-128">Módosíthatja ezt az objektumot, és a **set-AzureRmTrafficManagerProfile** használatával alkalmazhatja a változásokat a Traffic Managerben.</span><span class="sxs-lookup"><span data-stu-id="72909-128">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="72909-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72909-129">NOTES</span></span>

## <span data-ttu-id="72909-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72909-130">RELATED LINKS</span></span>

[<span data-ttu-id="72909-131">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72909-131">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="72909-132">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72909-132">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="72909-133">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72909-133">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="72909-134">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72909-134">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="72909-135">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72909-135">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


