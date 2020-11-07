---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 48d37bf19ec6613ce1f42ee8cf7609bd6383e12f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842810"
---
# <span data-ttu-id="d8725-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8725-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="d8725-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8725-102">SYNOPSIS</span></span>
<span data-ttu-id="d8725-103">Egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="d8725-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="d8725-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8725-104">SYNTAX</span></span>

### <span data-ttu-id="d8725-105">S1</span><span class="sxs-lookup"><span data-stu-id="d8725-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8725-106">S2</span><span class="sxs-lookup"><span data-stu-id="d8725-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8725-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8725-107">DESCRIPTION</span></span>
<span data-ttu-id="d8725-108">A **Get-AzAppServicePlan** parancsmag egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="d8725-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="d8725-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d8725-109">EXAMPLES</span></span>

### <span data-ttu-id="d8725-110">1. példa: alkalmazás-szolgáltatási terv beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="d8725-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="d8725-111">Ez a parancs beolvassa a ContosoASP nevű app-szolgáltatást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="d8725-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="d8725-112">2. példa: a minden alkalmazás-szolgáltatási csomag beszerzése egy helyre</span><span class="sxs-lookup"><span data-stu-id="d8725-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="d8725-113">Ez a parancs a "Nyugat-amerikai" régióban található összes app-szolgáltatási csomagot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="d8725-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="d8725-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8725-114">PARAMETERS</span></span>

### <span data-ttu-id="d8725-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8725-115">-DefaultProfile</span></span>
<span data-ttu-id="d8725-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8725-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8725-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="d8725-117">-Location</span></span>
<span data-ttu-id="d8725-118">Helyre</span><span class="sxs-lookup"><span data-stu-id="d8725-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8725-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d8725-119">-Name</span></span>
<span data-ttu-id="d8725-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="d8725-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8725-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8725-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8725-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d8725-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8725-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8725-123">CommonParameters</span></span>
<span data-ttu-id="d8725-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8725-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8725-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8725-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8725-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8725-126">INPUTS</span></span>

### <span data-ttu-id="d8725-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="d8725-127">None</span></span>
<span data-ttu-id="d8725-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d8725-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8725-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8725-129">OUTPUTS</span></span>

### <span data-ttu-id="d8725-130">Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="d8725-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="d8725-131">Microsoft. Azure. Management. WebSites. models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="d8725-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="d8725-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8725-132">NOTES</span></span>

## <span data-ttu-id="d8725-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8725-133">RELATED LINKS</span></span>

[<span data-ttu-id="d8725-134">Új – AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8725-134">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="d8725-135">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8725-135">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="d8725-136">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8725-136">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


