---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016512"
---
# <span data-ttu-id="a8dfb-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="a8dfb-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="a8dfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="a8dfb-103">Azure web hosting csomagok beolvasása az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="a8dfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8dfb-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8dfb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="a8dfb-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a8dfb-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a8dfb-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a8dfb-108">A **Get-AzureWebHostingPlan** parancsmag az Azure web hosting csomagokat az aktuális előfizetésben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="a8dfb-109">A **Get-AzureWebHostingPlan** alapértelmezés szerint az aktuális előfizetésben minden Azure-fogadási csomagot megkapja, és egy olyan objektumot ad eredményül, amely alapvető információkat nyújt a tervekről.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="a8dfb-110">A *tárhely* és a *név* paraméter használatakor a **Get-AzureWebHostingPlan** egy adott üzemeltetési terv objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="a8dfb-111">Az aktuális előfizetés megkereséséhez használja a **Get-AzureSubscription** parancsmag *aktuális* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="a8dfb-112">Az aktuális előfizetés módosításához használja a **Select-AzureSubscription** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="a8dfb-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a8dfb-113">EXAMPLES</span></span>

### <span data-ttu-id="a8dfb-114">Példa 1: az összes Webtárhely-csomag beszerzése előfizetésben</span><span class="sxs-lookup"><span data-stu-id="a8dfb-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="a8dfb-115">Ez a parancs beilleszti az összes Azure web hosting csomagot a jelenlegi előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="a8dfb-116">2. példa: speciális Webtárhely-csomag beszerzése előfizetésben</span><span class="sxs-lookup"><span data-stu-id="a8dfb-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="a8dfb-117">Ez a parancs beolvassa a Default0 nevű webtárhely csomagot a jelenlegi előfizetésben a westeuropewebspace nevű webtárhelyen.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="a8dfb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8dfb-118">PARAMETERS</span></span>

### <span data-ttu-id="a8dfb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8dfb-119">-Name</span></span>
<span data-ttu-id="a8dfb-120">Az előfizetésben szereplő terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="a8dfb-121">Ez a parancsmag alapértelmezés szerint a jelenlegi előfizetéshez tartozó összes csomagot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="a8dfb-122">Ez a paraméter nem támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-122">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8dfb-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8dfb-123">-Profile</span></span>
<span data-ttu-id="a8dfb-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8dfb-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dfb-126">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="a8dfb-126">-WebSpaceName</span></span>
<span data-ttu-id="a8dfb-127">Az előfizetésben lévő tárhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="a8dfb-128">Ez a parancsmag alapértelmezés szerint a megadott webtárhely összes webhelyét kapja.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="a8dfb-129">Ez a paraméter nem támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8dfb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8dfb-130">CommonParameters</span></span>
<span data-ttu-id="a8dfb-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8dfb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8dfb-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8dfb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8dfb-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8dfb-133">INPUTS</span></span>

###  
<span data-ttu-id="a8dfb-134">A parancsmagot név szerint, de nem érték szerint is továbbíthatja.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a8dfb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8dfb-135">OUTPUTS</span></span>

### <span data-ttu-id="a8dfb-136">Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. WebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="a8dfb-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="a8dfb-137">Alapértelmezés szerint a **Get-AzureWebHostingPlan** a **WebHostingPlan** -objektumok tömbjét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a8dfb-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="a8dfb-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8dfb-138">NOTES</span></span>

## <span data-ttu-id="a8dfb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8dfb-139">RELATED LINKS</span></span>

