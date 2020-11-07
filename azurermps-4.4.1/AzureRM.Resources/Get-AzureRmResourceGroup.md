---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679043"
---
# <span data-ttu-id="547a0-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="547a0-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="547a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="547a0-102">SYNOPSIS</span></span>
<span data-ttu-id="547a0-103">Erőforrás-csoportok beolvasása</span><span class="sxs-lookup"><span data-stu-id="547a0-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="547a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="547a0-104">SYNTAX</span></span>

### <span data-ttu-id="547a0-105">Felsorolja az erőforráscsoportot a név alapján.</span><span class="sxs-lookup"><span data-stu-id="547a0-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="547a0-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="547a0-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="547a0-107">Az azonosító alapján felsorolja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="547a0-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="547a0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="547a0-108">DESCRIPTION</span></span>
<span data-ttu-id="547a0-109">A **Get-AzureRmResourceGroup** parancsmag Azure-erőforráscsoportokat kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="547a0-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="547a0-110">Az összes erőforráscsoport beolvasható, vagy megadhat egy erőforráscsoportot név vagy egyéb tulajdonság alapján.</span><span class="sxs-lookup"><span data-stu-id="547a0-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="547a0-111">Alapértelmezés szerint ez a parancsmag a jelenlegi előfizetésben az összes erőforráscsoport számára elérhető lesz.</span><span class="sxs-lookup"><span data-stu-id="547a0-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="547a0-112">Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzureRmResourceGroup parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="547a0-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="547a0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="547a0-113">EXAMPLES</span></span>

### <span data-ttu-id="547a0-114">Példa 1: erőforráscsoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="547a0-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="547a0-115">Ez a parancs a EngineerBlog nevű előfizetésben az Azure Resource Group nevet kapja.</span><span class="sxs-lookup"><span data-stu-id="547a0-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="547a0-116">2. példa: erőforráscsoport összes címkéjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="547a0-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="547a0-117">Ez a parancs beolvassa a ContosoRG nevű erőforráscsoportot, és megjeleníti a csoporthoz társított címkéket.</span><span class="sxs-lookup"><span data-stu-id="547a0-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="547a0-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="547a0-118">PARAMETERS</span></span>

### <span data-ttu-id="547a0-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="547a0-119">-ApiVersion</span></span>
<span data-ttu-id="547a0-120">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="547a0-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="547a0-121">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="547a0-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="547a0-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="547a0-122">-Id</span></span>
<span data-ttu-id="547a0-123">A beolvasott erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="547a0-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="547a0-124">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="547a0-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547a0-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="547a0-125">-Location</span></span>
<span data-ttu-id="547a0-126">A beolvasott erőforráscsoport helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="547a0-126">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547a0-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="547a0-127">-Name</span></span>
<span data-ttu-id="547a0-128">A beolvasott erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="547a0-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="547a0-129">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="547a0-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547a0-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="547a0-130">-Pre</span></span>
<span data-ttu-id="547a0-131">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="547a0-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547a0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547a0-132">-DefaultProfile</span></span>
<span data-ttu-id="547a0-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="547a0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="547a0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547a0-134">CommonParameters</span></span>
<span data-ttu-id="547a0-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="547a0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547a0-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="547a0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547a0-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="547a0-137">INPUTS</span></span>

### <span data-ttu-id="547a0-138">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="547a0-138">String</span></span>
<span data-ttu-id="547a0-139">A parancsmagot tulajdonság neve szerint, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="547a0-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="547a0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="547a0-140">OUTPUTS</span></span>

### <span data-ttu-id="547a0-141">Microsoft. Azure. Command. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="547a0-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="547a0-142">Ez a parancsmag erőforrás-csoportokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="547a0-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="547a0-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="547a0-143">NOTES</span></span>

## <span data-ttu-id="547a0-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="547a0-144">RELATED LINKS</span></span>

[<span data-ttu-id="547a0-145">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="547a0-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="547a0-146">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="547a0-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="547a0-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="547a0-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


