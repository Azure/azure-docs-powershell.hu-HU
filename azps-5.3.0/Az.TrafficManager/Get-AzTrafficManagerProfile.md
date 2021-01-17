---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382869"
---
# <span data-ttu-id="55f3e-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="55f3e-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="55f3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="55f3e-103">Traffic Manager-profilt kap.</span><span class="sxs-lookup"><span data-stu-id="55f3e-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="55f3e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55f3e-104">SYNTAX</span></span>

### <span data-ttu-id="55f3e-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f3e-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55f3e-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f3e-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55f3e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55f3e-107">DESCRIPTION</span></span>
<span data-ttu-id="55f3e-108">A **Get-AzTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt kap, és visszaadja az adott profilt képviselő objektumot.</span><span class="sxs-lookup"><span data-stu-id="55f3e-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="55f3e-109">Adjon meg egy profilt a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="55f3e-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="55f3e-110">Ezt az objektumot helyben módosíthatja, majd a Set-AzTrafficManagerProfile alkalmazhatja a profilon.</span><span class="sxs-lookup"><span data-stu-id="55f3e-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="55f3e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55f3e-111">EXAMPLES</span></span>

### <span data-ttu-id="55f3e-112">1. példa: Profil létrehozása</span><span class="sxs-lookup"><span data-stu-id="55f3e-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="55f3e-113">Ez a parancs a ContosoProfile nevű profilt kapja meg az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="55f3e-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="55f3e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55f3e-114">PARAMETERS</span></span>

### <span data-ttu-id="55f3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f3e-115">-DefaultProfile</span></span>
<span data-ttu-id="55f3e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55f3e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55f3e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="55f3e-117">-Name</span></span>
<span data-ttu-id="55f3e-118">Megadja annak a Traffic Manager-profilnak a nevét, amelybe a parancsmagot beállítja.</span><span class="sxs-lookup"><span data-stu-id="55f3e-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55f3e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f3e-119">-ResourceGroupName</span></span>
<span data-ttu-id="55f3e-120">Annak az erőforráscsoportnak a nevét adja meg, amely tartalmazza a parancsmag által lekért Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="55f3e-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55f3e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f3e-121">CommonParameters</span></span>
<span data-ttu-id="55f3e-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f3e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f3e-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f3e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f3e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55f3e-124">INPUTS</span></span>

### <span data-ttu-id="55f3e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="55f3e-125">System.String</span></span>

## <span data-ttu-id="55f3e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55f3e-126">OUTPUTS</span></span>

### <span data-ttu-id="55f3e-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="55f3e-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="55f3e-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55f3e-128">NOTES</span></span>

## <span data-ttu-id="55f3e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55f3e-129">RELATED LINKS</span></span>

[<span data-ttu-id="55f3e-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="55f3e-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="55f3e-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="55f3e-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="55f3e-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="55f3e-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="55f3e-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="55f3e-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="55f3e-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="55f3e-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


