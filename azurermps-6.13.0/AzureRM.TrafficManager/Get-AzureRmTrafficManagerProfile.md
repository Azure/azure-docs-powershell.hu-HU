---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492687"
---
# <span data-ttu-id="37740-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="37740-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="37740-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37740-102">SYNOPSIS</span></span>
<span data-ttu-id="37740-103">Beolvassa a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="37740-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37740-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37740-104">SYNTAX</span></span>

### <span data-ttu-id="37740-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="37740-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37740-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="37740-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37740-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="37740-107">DESCRIPTION</span></span>
<span data-ttu-id="37740-108">A **Get-AzureRmTrafficManagerProfile** parancsmag Azure Traffic Manager-profilt kap, és egy olyan objektumot ad eredményül, amely a profilt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="37740-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="37740-109">Adjon meg egy profilt a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="37740-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="37740-110">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzureRmTrafficManagerProfile parancsmag használatával alkalmazhatja a profil módosításait.</span><span class="sxs-lookup"><span data-stu-id="37740-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="37740-111">Példák</span><span class="sxs-lookup"><span data-stu-id="37740-111">EXAMPLES</span></span>

### <span data-ttu-id="37740-112">Példa 1: profil beszerzése</span><span class="sxs-lookup"><span data-stu-id="37740-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="37740-113">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="37740-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="37740-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37740-114">PARAMETERS</span></span>

### <span data-ttu-id="37740-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37740-115">-DefaultProfile</span></span>
<span data-ttu-id="37740-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37740-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37740-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37740-117">-Name</span></span>
<span data-ttu-id="37740-118">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="37740-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37740-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37740-119">-ResourceGroupName</span></span>
<span data-ttu-id="37740-120">Annak a adatcsoportnak a neve, amely a parancsmag által beolvasott adatforgalmi vezető profilt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="37740-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37740-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37740-121">CommonParameters</span></span>
<span data-ttu-id="37740-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37740-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37740-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37740-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37740-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37740-124">INPUTS</span></span>

### <span data-ttu-id="37740-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="37740-125">None</span></span>
<span data-ttu-id="37740-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="37740-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37740-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37740-127">OUTPUTS</span></span>

### <span data-ttu-id="37740-128">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="37740-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="37740-129">Ez a parancsmag egy **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="37740-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="37740-130">Módosíthatja ezt az objektumot, és a **set-AzureRmTrafficManagerProfile** használatával alkalmazhatja a változásokat a Traffic Managerben.</span><span class="sxs-lookup"><span data-stu-id="37740-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="37740-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37740-131">NOTES</span></span>

## <span data-ttu-id="37740-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37740-132">RELATED LINKS</span></span>

[<span data-ttu-id="37740-133">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="37740-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="37740-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="37740-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="37740-135">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="37740-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="37740-136">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="37740-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="37740-137">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="37740-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


