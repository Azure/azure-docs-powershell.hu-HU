---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187951"
---
# <span data-ttu-id="e8541-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8541-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="e8541-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8541-102">SYNOPSIS</span></span>
<span data-ttu-id="e8541-103">Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="e8541-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="e8541-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8541-104">SYNTAX</span></span>

### <span data-ttu-id="e8541-105">S1</span><span class="sxs-lookup"><span data-stu-id="e8541-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8541-106">S2</span><span class="sxs-lookup"><span data-stu-id="e8541-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8541-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8541-107">DESCRIPTION</span></span>
<span data-ttu-id="e8541-108">A **Start-AzWebAppSlot** parancsmag egy Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="e8541-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="e8541-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e8541-109">EXAMPLES</span></span>

### <span data-ttu-id="e8541-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8541-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="e8541-111">Ez a parancs elindítja a Slot001 nevű, a ContosoWebApp nevű webalkalmazáshoz tartozó, a Default-Web-WestUS nevű erőforráscsoport nevű bővítőhelyet.</span><span class="sxs-lookup"><span data-stu-id="e8541-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e8541-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8541-112">PARAMETERS</span></span>

### <span data-ttu-id="e8541-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8541-113">-DefaultProfile</span></span>
<span data-ttu-id="e8541-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8541-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8541-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8541-115">-Name</span></span>
<span data-ttu-id="e8541-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e8541-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8541-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8541-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8541-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e8541-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8541-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="e8541-119">-Slot</span></span>
<span data-ttu-id="e8541-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="e8541-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8541-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e8541-121">-WebApp</span></span>
<span data-ttu-id="e8541-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="e8541-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8541-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8541-123">CommonParameters</span></span>
<span data-ttu-id="e8541-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8541-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8541-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8541-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8541-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8541-126">INPUTS</span></span>

### <span data-ttu-id="e8541-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e8541-127">System.String</span></span>

### <span data-ttu-id="e8541-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e8541-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e8541-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8541-129">OUTPUTS</span></span>

### <span data-ttu-id="e8541-130">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e8541-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e8541-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8541-131">NOTES</span></span>

## <span data-ttu-id="e8541-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8541-132">RELATED LINKS</span></span>

[<span data-ttu-id="e8541-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8541-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e8541-134">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8541-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="e8541-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8541-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="e8541-136">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8541-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="e8541-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8541-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="e8541-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8541-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="e8541-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e8541-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)