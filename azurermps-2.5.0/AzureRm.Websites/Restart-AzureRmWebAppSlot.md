---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: ad3ff3dbd5589a890ecf7649c9a9b66843b8b444
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850505"
---
# <span data-ttu-id="2c253-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c253-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="2c253-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c253-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c253-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c253-103">SYNTAX</span></span>

### <span data-ttu-id="2c253-104">S1</span><span class="sxs-lookup"><span data-stu-id="2c253-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c253-105">S2</span><span class="sxs-lookup"><span data-stu-id="2c253-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c253-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c253-106">DESCRIPTION</span></span>
<span data-ttu-id="2c253-107">Az **Újraindítás – AzureRmWebAppSlot** parancsmag leáll, majd egy Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="2c253-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="2c253-108">Ha a Web App a leállított állapotban van, használja az Start-AzureRmWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2c253-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="2c253-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2c253-109">EXAMPLES</span></span>

### <span data-ttu-id="2c253-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2c253-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="2c253-111">Ez a parancs elindítja a Slot001 a ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának bővítőhelyét – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="2c253-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2c253-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c253-112">PARAMETERS</span></span>

### <span data-ttu-id="2c253-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c253-113">-DefaultProfile</span></span>
<span data-ttu-id="2c253-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c253-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c253-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c253-115">-Name</span></span>
<span data-ttu-id="2c253-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="2c253-116">WebApp Name</span></span>

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

### <span data-ttu-id="2c253-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c253-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c253-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2c253-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2c253-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="2c253-119">-Slot</span></span>
<span data-ttu-id="2c253-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="2c253-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2c253-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2c253-121">-WebApp</span></span>
<span data-ttu-id="2c253-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="2c253-122">WebApp Object</span></span>

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

### <span data-ttu-id="2c253-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c253-123">CommonParameters</span></span>
<span data-ttu-id="2c253-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c253-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c253-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c253-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c253-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c253-126">INPUTS</span></span>

### <span data-ttu-id="2c253-127">Webhely</span><span class="sxs-lookup"><span data-stu-id="2c253-127">Site</span></span>
<span data-ttu-id="2c253-128">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2c253-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2c253-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c253-129">OUTPUTS</span></span>

## <span data-ttu-id="2c253-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c253-130">NOTES</span></span>

## <span data-ttu-id="2c253-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c253-131">RELATED LINKS</span></span>

[<span data-ttu-id="2c253-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c253-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c253-133">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c253-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c253-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c253-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c253-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c253-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c253-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c253-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c253-137">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c253-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c253-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2c253-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
