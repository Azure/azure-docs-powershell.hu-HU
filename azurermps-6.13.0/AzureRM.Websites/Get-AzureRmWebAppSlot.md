---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: f7be5b7877362484d0f3dfe4d19b8afc669e917c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491824"
---
# <span data-ttu-id="c09a4-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c09a4-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="c09a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c09a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c09a4-103">Azure Web App-bővítőhelyet kap.</span><span class="sxs-lookup"><span data-stu-id="c09a4-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c09a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c09a4-104">SYNTAX</span></span>

### <span data-ttu-id="c09a4-105">S1</span><span class="sxs-lookup"><span data-stu-id="c09a4-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c09a4-106">S2</span><span class="sxs-lookup"><span data-stu-id="c09a4-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c09a4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c09a4-107">DESCRIPTION</span></span>
<span data-ttu-id="c09a4-108">A **Get-AzureRmWebAppSlot** parancsmag információt kap egy Azure Web App-bővítőhelyről.</span><span class="sxs-lookup"><span data-stu-id="c09a4-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="c09a4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c09a4-109">EXAMPLES</span></span>

### <span data-ttu-id="c09a4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c09a4-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="c09a4-111">Ez a parancs beolvassa a Slot001 nevű bővítőhelyet a WebAppStandard nevű webalkalmazásból, amely az erőforráscsoport alapértelmezett – webes WestUS tartozik.</span><span class="sxs-lookup"><span data-stu-id="c09a4-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c09a4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c09a4-112">PARAMETERS</span></span>

### <span data-ttu-id="c09a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c09a4-113">-DefaultProfile</span></span>
<span data-ttu-id="c09a4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c09a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c09a4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c09a4-115">-Name</span></span>
<span data-ttu-id="c09a4-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c09a4-116">WebApp Name</span></span>

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

### <span data-ttu-id="c09a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c09a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="c09a4-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c09a4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c09a4-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="c09a4-119">-Slot</span></span>
<span data-ttu-id="c09a4-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="c09a4-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c09a4-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c09a4-121">-WebApp</span></span>
<span data-ttu-id="c09a4-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c09a4-122">WebApp Object</span></span>

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

### <span data-ttu-id="c09a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c09a4-123">CommonParameters</span></span>
<span data-ttu-id="c09a4-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c09a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c09a4-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c09a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c09a4-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c09a4-126">INPUTS</span></span>

### <span data-ttu-id="c09a4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c09a4-127">System.String</span></span>

### <span data-ttu-id="c09a4-128">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="c09a4-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c09a4-129">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c09a4-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c09a4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c09a4-130">OUTPUTS</span></span>

### <span data-ttu-id="c09a4-131">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="c09a4-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c09a4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c09a4-132">NOTES</span></span>

## <span data-ttu-id="c09a4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c09a4-133">RELATED LINKS</span></span>

[<span data-ttu-id="c09a4-134">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c09a4-134">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="c09a4-135">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c09a4-135">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="c09a4-136">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c09a4-136">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="c09a4-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c09a4-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="c09a4-138">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c09a4-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="c09a4-139">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c09a4-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="c09a4-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c09a4-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
