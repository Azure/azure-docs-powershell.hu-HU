---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194978"
---
# <span data-ttu-id="7e3ba-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="7e3ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3ba-103">Lehetővé teszi a forgalomirányítási profilok betöltését.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="7e3ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e3ba-104">SYNTAX</span></span>

### <span data-ttu-id="7e3ba-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="7e3ba-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e3ba-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="7e3ba-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e3ba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e3ba-107">DESCRIPTION</span></span>
<span data-ttu-id="7e3ba-108">Az **enable-AzTrafficManagerProfile** parancsmag az Azure Traffic Manager-profil engedélyezését teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7e3ba-109">Megadhatja a profil objektumát a csővezeték vagy a paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="7e3ba-110">Azt is megteheti, hogy a *név* és a *ResourceGroupName* paraméterrel megadhatja a profilt.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="7e3ba-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7e3ba-111">EXAMPLES</span></span>

### <span data-ttu-id="7e3ba-112">1. példa: név szerint megadott profil engedélyezése</span><span class="sxs-lookup"><span data-stu-id="7e3ba-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7e3ba-113">Ez a parancs engedélyezi a ContosoProfile nevű profilt a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="7e3ba-114">2. példa: profil engedélyezése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="7e3ba-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="7e3ba-115">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7e3ba-116">Ekkor a parancs átadja ezt a profilt az **enable-AzTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e3ba-117">Ez a parancsmag engedélyezi ezt a profilt.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="7e3ba-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e3ba-118">PARAMETERS</span></span>

### <span data-ttu-id="7e3ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-119">-DefaultProfile</span></span>
<span data-ttu-id="7e3ba-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e3ba-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e3ba-121">-Name</span></span>
<span data-ttu-id="7e3ba-122">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre ez a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="7e3ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e3ba-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7e3ba-125">Ez a parancsmag lehetővé teszi a forgalomirányító profilját abban a csoportban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e3ba-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="7e3ba-127">Megadja az engedélyezni kívánt **TrafficManagerProfile** objektumot.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="7e3ba-128">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7e3ba-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="7e3ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3ba-129">CommonParameters</span></span>
<span data-ttu-id="7e3ba-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e3ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3ba-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e3ba-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3ba-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e3ba-132">INPUTS</span></span>

### <span data-ttu-id="7e3ba-133">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7e3ba-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e3ba-134">OUTPUTS</span></span>

### <span data-ttu-id="7e3ba-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e3ba-135">System.Boolean</span></span>

## <span data-ttu-id="7e3ba-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e3ba-136">NOTES</span></span>

## <span data-ttu-id="7e3ba-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e3ba-137">RELATED LINKS</span></span>

[<span data-ttu-id="7e3ba-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e3ba-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e3ba-140">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e3ba-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e3ba-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ba-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

