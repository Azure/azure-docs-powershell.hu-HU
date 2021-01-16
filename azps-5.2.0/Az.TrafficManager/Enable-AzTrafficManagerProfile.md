---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326195"
---
# <span data-ttu-id="4ed8c-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="4ed8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed8c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed8c-103">Engedélyezi a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="4ed8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ed8c-104">SYNTAX</span></span>

### <span data-ttu-id="4ed8c-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="4ed8c-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ed8c-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="4ed8c-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed8c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ed8c-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed8c-108">Az **Enable-AzTrafficManagerProfile** parancsmag engedélyezi az Azure Traffic Manager-profilokat.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="4ed8c-109">A profilobjektumot a folyamat használatával vagy paraméterértékként adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="4ed8c-110">Másik lehetőségként a Name és  az *ResourceGroupName* paraméter használatával is megadhatja a profilt.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="4ed8c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ed8c-111">EXAMPLES</span></span>

### <span data-ttu-id="4ed8c-112">1. példa: Névvel megadott profil engedélyezése</span><span class="sxs-lookup"><span data-stu-id="4ed8c-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="4ed8c-113">Ez a parancs engedélyezi a ContosoProfile nevű profilt az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="4ed8c-114">2. példa: Profil engedélyezése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="4ed8c-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="4ed8c-115">Ez a parancs a ContosoProfile nevű profilt kapja meg az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="4ed8c-116">A parancs ezután átadja a profilt az **Enable-AzTrafficManagerProfile** parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4ed8c-117">Ez a parancsmag engedélyezi ezt a profilt.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="4ed8c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ed8c-118">PARAMETERS</span></span>

### <span data-ttu-id="4ed8c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-119">-DefaultProfile</span></span>
<span data-ttu-id="4ed8c-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed8c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4ed8c-121">-Name</span></span>
<span data-ttu-id="4ed8c-122">Az a Traffic Manager-profil neve, amely ezt a parancsmagot engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="4ed8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ed8c-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4ed8c-125">Ez a parancsmag engedélyezi a Traffic Manager-profilt abban a csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ed8c-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="4ed8c-127">Engedélyezi a **TrafficManagerProfile** objektumot.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="4ed8c-128">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="4ed8c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed8c-129">CommonParameters</span></span>
<span data-ttu-id="4ed8c-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed8c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed8c-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed8c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed8c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ed8c-132">INPUTS</span></span>

### <span data-ttu-id="4ed8c-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4ed8c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ed8c-134">OUTPUTS</span></span>

### <span data-ttu-id="4ed8c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ed8c-135">System.Boolean</span></span>

## <span data-ttu-id="4ed8c-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ed8c-136">NOTES</span></span>

## <span data-ttu-id="4ed8c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ed8c-137">RELATED LINKS</span></span>

[<span data-ttu-id="4ed8c-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="4ed8c-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="4ed8c-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="4ed8c-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="4ed8c-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed8c-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


