---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187902"
---
# <span data-ttu-id="fb07a-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb07a-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="fb07a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb07a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb07a-103">Beolvassa a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="fb07a-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="fb07a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb07a-104">SYNTAX</span></span>

### <span data-ttu-id="fb07a-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb07a-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb07a-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb07a-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb07a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb07a-107">DESCRIPTION</span></span>
<span data-ttu-id="fb07a-108">A **Get-AzTrafficManagerProfile** parancsmag Azure Traffic Manager-profilt kap, és egy olyan objektumot ad eredményül, amely a profilt jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fb07a-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="fb07a-109">Adjon meg egy profilt a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="fb07a-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="fb07a-110">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzTrafficManagerProfile parancsmag használatával alkalmazhatja a profil módosításait.</span><span class="sxs-lookup"><span data-stu-id="fb07a-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="fb07a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fb07a-111">EXAMPLES</span></span>

### <span data-ttu-id="fb07a-112">Példa 1: profil beszerzése</span><span class="sxs-lookup"><span data-stu-id="fb07a-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="fb07a-113">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="fb07a-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="fb07a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb07a-114">PARAMETERS</span></span>

### <span data-ttu-id="fb07a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb07a-115">-DefaultProfile</span></span>
<span data-ttu-id="fb07a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb07a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb07a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb07a-117">-Name</span></span>
<span data-ttu-id="fb07a-118">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="fb07a-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb07a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb07a-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb07a-120">Annak a adatcsoportnak a neve, amely a parancsmag által beolvasott adatforgalmi vezető profilt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fb07a-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb07a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb07a-121">CommonParameters</span></span>
<span data-ttu-id="fb07a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb07a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb07a-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb07a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb07a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb07a-124">INPUTS</span></span>

### <span data-ttu-id="fb07a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fb07a-125">System.String</span></span>

## <span data-ttu-id="fb07a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb07a-126">OUTPUTS</span></span>

### <span data-ttu-id="fb07a-127">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb07a-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="fb07a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb07a-128">NOTES</span></span>

## <span data-ttu-id="fb07a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb07a-129">RELATED LINKS</span></span>

[<span data-ttu-id="fb07a-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb07a-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="fb07a-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb07a-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="fb07a-132">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb07a-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="fb07a-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb07a-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="fb07a-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb07a-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


