---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842673"
---
# <span data-ttu-id="d37d5-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37d5-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="d37d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d37d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d37d5-103">Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="d37d5-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="d37d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d37d5-104">SYNTAX</span></span>

### <span data-ttu-id="d37d5-105">S1</span><span class="sxs-lookup"><span data-stu-id="d37d5-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d37d5-106">S2</span><span class="sxs-lookup"><span data-stu-id="d37d5-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d37d5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d37d5-107">DESCRIPTION</span></span>
<span data-ttu-id="d37d5-108">A **Start-AzWebAppSlot** parancsmag egy Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="d37d5-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="d37d5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d37d5-109">EXAMPLES</span></span>

### <span data-ttu-id="d37d5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d37d5-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d37d5-111">Ez a parancs elindítja a Slot001 nevű, a ContosoWebApp nevű webalkalmazáshoz tartozó, a Default-Web-WestUS nevű erőforráscsoport nevű bővítőhelyet.</span><span class="sxs-lookup"><span data-stu-id="d37d5-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d37d5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d37d5-112">PARAMETERS</span></span>

### <span data-ttu-id="d37d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37d5-113">-DefaultProfile</span></span>
<span data-ttu-id="d37d5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d37d5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d37d5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d37d5-115">-Name</span></span>
<span data-ttu-id="d37d5-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="d37d5-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37d5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37d5-117">-ResourceGroupName</span></span>
<span data-ttu-id="d37d5-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d37d5-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37d5-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="d37d5-119">-Slot</span></span>
<span data-ttu-id="d37d5-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="d37d5-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37d5-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d37d5-121">-WebApp</span></span>
<span data-ttu-id="d37d5-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="d37d5-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d37d5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37d5-123">CommonParameters</span></span>
<span data-ttu-id="d37d5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d37d5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37d5-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37d5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37d5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37d5-126">INPUTS</span></span>

### <span data-ttu-id="d37d5-127">Webhely</span><span class="sxs-lookup"><span data-stu-id="d37d5-127">Site</span></span>
<span data-ttu-id="d37d5-128">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d37d5-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d37d5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37d5-129">OUTPUTS</span></span>

## <span data-ttu-id="d37d5-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d37d5-130">NOTES</span></span>

## <span data-ttu-id="d37d5-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d37d5-131">RELATED LINKS</span></span>

[<span data-ttu-id="d37d5-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37d5-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d37d5-133">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37d5-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d37d5-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37d5-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d37d5-135">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37d5-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="d37d5-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37d5-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="d37d5-137">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37d5-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d37d5-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d37d5-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
