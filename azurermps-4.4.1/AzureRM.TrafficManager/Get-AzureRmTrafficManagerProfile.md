---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 6be04cea9e3e73a06cdbb1ee449adaefd4fe803e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680460"
---
# <span data-ttu-id="dc643-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc643-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="dc643-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc643-102">SYNOPSIS</span></span>
<span data-ttu-id="dc643-103">Beolvassa a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="dc643-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc643-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc643-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc643-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc643-105">DESCRIPTION</span></span>
<span data-ttu-id="dc643-106">A **Get-AzureRmTrafficManagerProfile** parancsmag Azure Traffic Manager-profilt kap, és egy olyan objektumot ad eredményül, amely a profilt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="dc643-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="dc643-107">Adjon meg egy profilt a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="dc643-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="dc643-108">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzureRmTrafficManagerProfile parancsmag használatával alkalmazhatja a profil módosításait.</span><span class="sxs-lookup"><span data-stu-id="dc643-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="dc643-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dc643-109">EXAMPLES</span></span>

### <span data-ttu-id="dc643-110">Példa 1: profil beszerzése</span><span class="sxs-lookup"><span data-stu-id="dc643-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="dc643-111">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="dc643-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="dc643-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc643-112">PARAMETERS</span></span>

### <span data-ttu-id="dc643-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc643-113">-Name</span></span>
<span data-ttu-id="dc643-114">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="dc643-114">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc643-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc643-115">-ResourceGroupName</span></span>
<span data-ttu-id="dc643-116">Annak a adatcsoportnak a neve, amely a parancsmag által beolvasott adatforgalmi vezető profilt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dc643-116">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc643-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc643-117">-DefaultProfile</span></span>
<span data-ttu-id="dc643-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc643-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc643-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc643-119">CommonParameters</span></span>
<span data-ttu-id="dc643-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc643-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc643-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc643-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc643-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc643-122">INPUTS</span></span>

## <span data-ttu-id="dc643-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc643-123">OUTPUTS</span></span>

### <span data-ttu-id="dc643-124">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc643-124">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="dc643-125">Ez a parancsmag egy **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dc643-125">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="dc643-126">Módosíthatja ezt az objektumot, és a **set-AzureRmTrafficManagerProfile** használatával alkalmazhatja a változásokat a Traffic Managerben.</span><span class="sxs-lookup"><span data-stu-id="dc643-126">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="dc643-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc643-127">NOTES</span></span>

## <span data-ttu-id="dc643-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc643-128">RELATED LINKS</span></span>

[<span data-ttu-id="dc643-129">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc643-129">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="dc643-130">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc643-130">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="dc643-131">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc643-131">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="dc643-132">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc643-132">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="dc643-133">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc643-133">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


