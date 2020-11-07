---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842761"
---
# <span data-ttu-id="c30ee-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c30ee-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="c30ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c30ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c30ee-103">Azure Web App-bővítőhelyet kap.</span><span class="sxs-lookup"><span data-stu-id="c30ee-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="c30ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c30ee-104">SYNTAX</span></span>

### <span data-ttu-id="c30ee-105">S1</span><span class="sxs-lookup"><span data-stu-id="c30ee-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c30ee-106">S2</span><span class="sxs-lookup"><span data-stu-id="c30ee-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c30ee-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c30ee-107">DESCRIPTION</span></span>
<span data-ttu-id="c30ee-108">A **Get-AzWebAppSlot** parancsmag információt kap egy Azure Web App-bővítőhelyről.</span><span class="sxs-lookup"><span data-stu-id="c30ee-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="c30ee-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c30ee-109">EXAMPLES</span></span>

### <span data-ttu-id="c30ee-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c30ee-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="c30ee-111">Ez a parancs beolvassa a Slot001 nevű bővítőhelyet a WebAppStandard nevű webalkalmazásból, amely az erőforráscsoport alapértelmezett – webes WestUS tartozik.</span><span class="sxs-lookup"><span data-stu-id="c30ee-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c30ee-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c30ee-112">PARAMETERS</span></span>

### <span data-ttu-id="c30ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30ee-113">-DefaultProfile</span></span>
<span data-ttu-id="c30ee-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c30ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c30ee-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c30ee-115">-Name</span></span>
<span data-ttu-id="c30ee-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c30ee-116">WebApp Name</span></span>

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

### <span data-ttu-id="c30ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="c30ee-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c30ee-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c30ee-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="c30ee-119">-Slot</span></span>
<span data-ttu-id="c30ee-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="c30ee-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30ee-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c30ee-121">-WebApp</span></span>
<span data-ttu-id="c30ee-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c30ee-122">WebApp Object</span></span>

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

### <span data-ttu-id="c30ee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30ee-123">CommonParameters</span></span>
<span data-ttu-id="c30ee-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c30ee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30ee-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c30ee-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30ee-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c30ee-126">INPUTS</span></span>

### <span data-ttu-id="c30ee-127">Webhely</span><span class="sxs-lookup"><span data-stu-id="c30ee-127">Site</span></span>
<span data-ttu-id="c30ee-128">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c30ee-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c30ee-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c30ee-129">OUTPUTS</span></span>

## <span data-ttu-id="c30ee-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c30ee-130">NOTES</span></span>

## <span data-ttu-id="c30ee-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c30ee-131">RELATED LINKS</span></span>

[<span data-ttu-id="c30ee-132">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c30ee-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c30ee-133">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c30ee-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c30ee-134">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c30ee-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="c30ee-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c30ee-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="c30ee-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c30ee-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c30ee-137">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c30ee-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c30ee-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c30ee-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
