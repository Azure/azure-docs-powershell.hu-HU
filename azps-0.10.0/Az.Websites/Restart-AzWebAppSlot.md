---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842685"
---
# <span data-ttu-id="2f0d9-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f0d9-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="2f0d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f0d9-102">SYNOPSIS</span></span>

## <span data-ttu-id="2f0d9-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f0d9-103">SYNTAX</span></span>

### <span data-ttu-id="2f0d9-104">S1</span><span class="sxs-lookup"><span data-stu-id="2f0d9-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0d9-105">S2</span><span class="sxs-lookup"><span data-stu-id="2f0d9-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f0d9-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f0d9-106">DESCRIPTION</span></span>
<span data-ttu-id="2f0d9-107">Az **Újraindítás – AzWebAppSlot** parancsmag leáll, majd egy Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="2f0d9-108">Ha a Web App a leállított állapotban van, használja az Start-AzWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="2f0d9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2f0d9-109">EXAMPLES</span></span>

### <span data-ttu-id="2f0d9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f0d9-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="2f0d9-111">Ez a parancs elindítja a Slot001 a ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának bővítőhelyét – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="2f0d9-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2f0d9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f0d9-112">PARAMETERS</span></span>

### <span data-ttu-id="2f0d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0d9-113">-DefaultProfile</span></span>
<span data-ttu-id="2f0d9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f0d9-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f0d9-115">-Name</span></span>
<span data-ttu-id="2f0d9-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="2f0d9-116">WebApp Name</span></span>

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

### <span data-ttu-id="2f0d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f0d9-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2f0d9-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2f0d9-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="2f0d9-119">-Slot</span></span>
<span data-ttu-id="2f0d9-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="2f0d9-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2f0d9-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2f0d9-121">-WebApp</span></span>
<span data-ttu-id="2f0d9-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="2f0d9-122">WebApp Object</span></span>

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

### <span data-ttu-id="2f0d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0d9-123">CommonParameters</span></span>
<span data-ttu-id="2f0d9-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f0d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0d9-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f0d9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0d9-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f0d9-126">INPUTS</span></span>

### <span data-ttu-id="2f0d9-127">Webhely</span><span class="sxs-lookup"><span data-stu-id="2f0d9-127">Site</span></span>
<span data-ttu-id="2f0d9-128">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2f0d9-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2f0d9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f0d9-129">OUTPUTS</span></span>

## <span data-ttu-id="2f0d9-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f0d9-130">NOTES</span></span>

## <span data-ttu-id="2f0d9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f0d9-131">RELATED LINKS</span></span>

[<span data-ttu-id="2f0d9-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f0d9-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2f0d9-133">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f0d9-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="2f0d9-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f0d9-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="2f0d9-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f0d9-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="2f0d9-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f0d9-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="2f0d9-137">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f0d9-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="2f0d9-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2f0d9-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
