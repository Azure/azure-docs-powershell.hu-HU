---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 08e5f0e1ba87f42f8a2893a63f8f853ece9870c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679235"
---
# <span data-ttu-id="4baca-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4baca-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="4baca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4baca-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4baca-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4baca-103">SYNTAX</span></span>

### <span data-ttu-id="4baca-104">S1</span><span class="sxs-lookup"><span data-stu-id="4baca-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4baca-105">S2</span><span class="sxs-lookup"><span data-stu-id="4baca-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4baca-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="4baca-106">DESCRIPTION</span></span>
<span data-ttu-id="4baca-107">Az **Újraindítás – AzureRmWebAppSlot** parancsmag leáll, majd egy Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="4baca-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="4baca-108">Ha a Web App a leállított állapotban van, használja az Start-AzureRmWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4baca-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="4baca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4baca-109">EXAMPLES</span></span>

### <span data-ttu-id="4baca-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4baca-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="4baca-111">Ez a parancs elindítja a Slot001 a ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának bővítőhelyét – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="4baca-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4baca-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4baca-112">PARAMETERS</span></span>

### <span data-ttu-id="4baca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4baca-113">-DefaultProfile</span></span>
<span data-ttu-id="4baca-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4baca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4baca-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4baca-115">-Name</span></span>
<span data-ttu-id="4baca-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="4baca-116">WebApp Name</span></span>

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

### <span data-ttu-id="4baca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4baca-117">-ResourceGroupName</span></span>
<span data-ttu-id="4baca-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4baca-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4baca-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="4baca-119">-Slot</span></span>
<span data-ttu-id="4baca-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="4baca-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="4baca-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4baca-121">-WebApp</span></span>
<span data-ttu-id="4baca-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="4baca-122">WebApp Object</span></span>

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

### <span data-ttu-id="4baca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4baca-123">CommonParameters</span></span>
<span data-ttu-id="4baca-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4baca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4baca-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4baca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4baca-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4baca-126">INPUTS</span></span>

### <span data-ttu-id="4baca-127">Webhely</span><span class="sxs-lookup"><span data-stu-id="4baca-127">Site</span></span>
<span data-ttu-id="4baca-128">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4baca-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4baca-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4baca-129">OUTPUTS</span></span>

## <span data-ttu-id="4baca-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4baca-130">NOTES</span></span>

## <span data-ttu-id="4baca-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4baca-131">RELATED LINKS</span></span>

[<span data-ttu-id="4baca-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4baca-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="4baca-133">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4baca-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="4baca-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4baca-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="4baca-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4baca-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="4baca-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4baca-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="4baca-137">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4baca-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="4baca-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4baca-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
