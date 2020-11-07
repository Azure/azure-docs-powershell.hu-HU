---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 3dd86c186d05ce59f237be51b8e059e800c47a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678944"
---
# <span data-ttu-id="96dbf-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="96dbf-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="96dbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="96dbf-103">Felügyelt alkalmazásokat kap</span><span class="sxs-lookup"><span data-stu-id="96dbf-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96dbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96dbf-104">SYNTAX</span></span>

### <span data-ttu-id="96dbf-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96dbf-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96dbf-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96dbf-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96dbf-107">GetById</span><span class="sxs-lookup"><span data-stu-id="96dbf-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96dbf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="96dbf-108">DESCRIPTION</span></span>
<span data-ttu-id="96dbf-109">A **Get-AzureRmManagedApplication** parancsmag felügyelt alkalmazásokat kap</span><span class="sxs-lookup"><span data-stu-id="96dbf-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="96dbf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="96dbf-110">EXAMPLES</span></span>

### <span data-ttu-id="96dbf-111">Példa 1: az összes felügyelt alkalmazás beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="96dbf-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="96dbf-112">A parancs a kezelt alkalmazásokat a "MyRG" erőforráscsoport alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="96dbf-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="96dbf-113">2. példa: az összes felügyelt alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="96dbf-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="96dbf-114">Ez a parancs beolvassa az összes felügyelt alkalmazást az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="96dbf-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="96dbf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96dbf-115">PARAMETERS</span></span>

### <span data-ttu-id="96dbf-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="96dbf-116">-ApiVersion</span></span>
<span data-ttu-id="96dbf-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="96dbf-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="96dbf-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="96dbf-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="96dbf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96dbf-119">-DefaultProfile</span></span>
<span data-ttu-id="96dbf-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96dbf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96dbf-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="96dbf-121">-Id</span></span>
<span data-ttu-id="96dbf-122">A teljes mértékben minősített felügyelt alkalmazásspecifikus azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="96dbf-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="96dbf-123">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="96dbf-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96dbf-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96dbf-124">-Name</span></span>
<span data-ttu-id="96dbf-125">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="96dbf-125">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96dbf-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="96dbf-126">-Pre</span></span>
<span data-ttu-id="96dbf-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="96dbf-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96dbf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96dbf-128">-ResourceGroupName</span></span>
<span data-ttu-id="96dbf-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="96dbf-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96dbf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96dbf-130">CommonParameters</span></span>
<span data-ttu-id="96dbf-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96dbf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96dbf-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96dbf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96dbf-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96dbf-133">INPUTS</span></span>

### <span data-ttu-id="96dbf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="96dbf-134">System.String</span></span>

## <span data-ttu-id="96dbf-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96dbf-135">OUTPUTS</span></span>

### <span data-ttu-id="96dbf-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="96dbf-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="96dbf-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96dbf-137">NOTES</span></span>

## <span data-ttu-id="96dbf-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96dbf-138">RELATED LINKS</span></span>
