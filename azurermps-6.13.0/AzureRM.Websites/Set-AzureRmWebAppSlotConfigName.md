---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 75c134b162636f94b00cf6692f4e9df120930dcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497136"
---
# <span data-ttu-id="74ae9-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="74ae9-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="74ae9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="74ae9-103">A Web App-bővítőhely konfigurációs neveinek beállítása</span><span class="sxs-lookup"><span data-stu-id="74ae9-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74ae9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74ae9-104">SYNTAX</span></span>

### <span data-ttu-id="74ae9-105">S1</span><span class="sxs-lookup"><span data-stu-id="74ae9-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74ae9-106">S2</span><span class="sxs-lookup"><span data-stu-id="74ae9-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74ae9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="74ae9-107">DESCRIPTION</span></span>
<span data-ttu-id="74ae9-108">A **set-AzureRmWebAppSlotConfigName** parancsmag az App beállításait és a csatlakozási karakterláncokat bővítőhelyként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="74ae9-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="74ae9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="74ae9-109">EXAMPLES</span></span>

### <span data-ttu-id="74ae9-110">1:</span><span class="sxs-lookup"><span data-stu-id="74ae9-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="74ae9-111">Ez a parancs eltávolítja a webalkalmazások ContosoWebApp társított összes app-beállítást és a kapcsolati karakterláncot az erőforráscsoport alapértelmezett verziójában – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="74ae9-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="74ae9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74ae9-112">PARAMETERS</span></span>

### <span data-ttu-id="74ae9-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="74ae9-113">-AppSettingNames</span></span>
<span data-ttu-id="74ae9-114">Az alkalmazás beállításai nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="74ae9-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ae9-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="74ae9-115">-ConnectionStringNames</span></span>
<span data-ttu-id="74ae9-116">A kapcsolati karakterláncok nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="74ae9-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ae9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ae9-117">-DefaultProfile</span></span>
<span data-ttu-id="74ae9-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74ae9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74ae9-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74ae9-119">-Name</span></span>
<span data-ttu-id="74ae9-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="74ae9-120">WebApp Name</span></span>

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

### <span data-ttu-id="74ae9-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="74ae9-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="74ae9-122">Az összes app-név eltávolítása beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="74ae9-122">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ae9-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="74ae9-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="74ae9-124">Az összes kapcsolati karakterlánc nevének eltávolítása beállítás</span><span class="sxs-lookup"><span data-stu-id="74ae9-124">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ae9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74ae9-125">-ResourceGroupName</span></span>
<span data-ttu-id="74ae9-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="74ae9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="74ae9-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="74ae9-127">-WebApp</span></span>
<span data-ttu-id="74ae9-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="74ae9-128">WebApp Object</span></span>

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

### <span data-ttu-id="74ae9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ae9-129">CommonParameters</span></span>
<span data-ttu-id="74ae9-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74ae9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ae9-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ae9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ae9-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74ae9-132">INPUTS</span></span>

### <span data-ttu-id="74ae9-133">System. string []</span><span class="sxs-lookup"><span data-stu-id="74ae9-133">System.String[]</span></span>

### <span data-ttu-id="74ae9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="74ae9-134">System.String</span></span>

### <span data-ttu-id="74ae9-135">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="74ae9-135">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="74ae9-136">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74ae9-136">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="74ae9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74ae9-137">OUTPUTS</span></span>

### <span data-ttu-id="74ae9-138">Microsoft. Azure. Management. WebSites. models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="74ae9-138">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="74ae9-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74ae9-139">NOTES</span></span>

## <span data-ttu-id="74ae9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74ae9-140">RELATED LINKS</span></span>
