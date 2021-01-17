---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330389"
---
# <span data-ttu-id="1019a-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="1019a-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="1019a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1019a-102">SYNOPSIS</span></span>
<span data-ttu-id="1019a-103">Eltávolít egy végpontot egy helyi Traffic Manager-profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="1019a-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="1019a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1019a-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1019a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1019a-105">DESCRIPTION</span></span>
<span data-ttu-id="1019a-106">A **Remove-AzTrafficManagerEndpointConfig** parancsmag eltávolít egy végpontot egy helyi Azure Traffic Manager-profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="1019a-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="1019a-107">A profilt a Get-AzTrafficManagerProfile használhatja.</span><span class="sxs-lookup"><span data-stu-id="1019a-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="1019a-108">Ez a parancsmag a helyi profilobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="1019a-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="1019a-109">A Forgalomkezelőben a módosításokat a Set-AzTrafficManagerProfile el.</span><span class="sxs-lookup"><span data-stu-id="1019a-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="1019a-110">Egy végpont eltávolításához és a módosítások egyetlen műveletben való véglegesítéshez használja a Remove-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1019a-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="1019a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1019a-111">EXAMPLES</span></span>

### <span data-ttu-id="1019a-112">1. példa: Végpont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1019a-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="1019a-113">Az első parancs a **Get-AzTrafficManagerProfile** parancsmag használatával kap egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="1019a-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="1019a-114">A parancs a helyi profilt a $TrafficManagerProfile tárolja.</span><span class="sxs-lookup"><span data-stu-id="1019a-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="1019a-115">A második parancs eltávolítja a contoso nevű Azure-végpontot a $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1019a-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="1019a-116">Ez a parancs csak a helyi objektumot módosítja.</span><span class="sxs-lookup"><span data-stu-id="1019a-116">This command changes only the local object.</span></span>

<span data-ttu-id="1019a-117">Az utolsó parancs frissíti a ContosoProfile nevű Forgalomkezelő-profilt, hogy megfeleljen a helyi $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1019a-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="1019a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1019a-118">PARAMETERS</span></span>

### <span data-ttu-id="1019a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1019a-119">-DefaultProfile</span></span>
<span data-ttu-id="1019a-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1019a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1019a-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1019a-121">-EndpointName</span></span>
<span data-ttu-id="1019a-122">Annak a Traffic Manager-végpontnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="1019a-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1019a-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1019a-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="1019a-124">Helyi **TrafficManagerProfile objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="1019a-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1019a-125">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="1019a-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="1019a-126">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1019a-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="1019a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1019a-127">CommonParameters</span></span>
<span data-ttu-id="1019a-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1019a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1019a-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1019a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1019a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1019a-130">INPUTS</span></span>

### <span data-ttu-id="1019a-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1019a-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1019a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1019a-132">OUTPUTS</span></span>

### <span data-ttu-id="1019a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1019a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1019a-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1019a-134">NOTES</span></span>

## <span data-ttu-id="1019a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1019a-135">RELATED LINKS</span></span>

[<span data-ttu-id="1019a-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="1019a-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="1019a-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1019a-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="1019a-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1019a-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1019a-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1019a-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


