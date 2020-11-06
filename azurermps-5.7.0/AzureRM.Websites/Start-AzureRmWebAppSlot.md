---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: e9b0fa9f492c64f86668688d12171795735a46dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492107"
---
# <span data-ttu-id="bc663-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bc663-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="bc663-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc663-102">SYNOPSIS</span></span>
<span data-ttu-id="bc663-103">Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="bc663-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc663-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc663-104">SYNTAX</span></span>

### <span data-ttu-id="bc663-105">S1</span><span class="sxs-lookup"><span data-stu-id="bc663-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc663-106">S2</span><span class="sxs-lookup"><span data-stu-id="bc663-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc663-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc663-107">DESCRIPTION</span></span>
<span data-ttu-id="bc663-108">A **Start-AzureRmWebAppSlot** parancsmag egy Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="bc663-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="bc663-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bc663-109">EXAMPLES</span></span>

### <span data-ttu-id="bc663-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bc663-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="bc663-111">Ez a parancs elindítja a Slot001 nevű, a ContosoWebApp nevű webalkalmazáshoz tartozó, a Default-Web-WestUS nevű erőforráscsoport nevű bővítőhelyet.</span><span class="sxs-lookup"><span data-stu-id="bc663-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bc663-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc663-112">PARAMETERS</span></span>

### <span data-ttu-id="bc663-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc663-113">-DefaultProfile</span></span>
<span data-ttu-id="bc663-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc663-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc663-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc663-115">-Name</span></span>
<span data-ttu-id="bc663-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="bc663-116">WebApp Name</span></span>

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

### <span data-ttu-id="bc663-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc663-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc663-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="bc663-118">Resource Group Name</span></span>

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

### <span data-ttu-id="bc663-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="bc663-119">-Slot</span></span>
<span data-ttu-id="bc663-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="bc663-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bc663-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bc663-121">-WebApp</span></span>
<span data-ttu-id="bc663-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="bc663-122">WebApp Object</span></span>

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

### <span data-ttu-id="bc663-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc663-123">CommonParameters</span></span>
<span data-ttu-id="bc663-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc663-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc663-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc663-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc663-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc663-126">INPUTS</span></span>

### <span data-ttu-id="bc663-127">Webhely</span><span class="sxs-lookup"><span data-stu-id="bc663-127">Site</span></span>
<span data-ttu-id="bc663-128">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bc663-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bc663-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc663-129">OUTPUTS</span></span>

## <span data-ttu-id="bc663-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc663-130">NOTES</span></span>

## <span data-ttu-id="bc663-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc663-131">RELATED LINKS</span></span>

[<span data-ttu-id="bc663-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bc663-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="bc663-133">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bc663-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="bc663-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bc663-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="bc663-135">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bc663-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="bc663-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bc663-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="bc663-137">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bc663-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="bc663-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bc663-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
