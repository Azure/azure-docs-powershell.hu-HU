---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: 5e2b13cd4c2586b15cc526aad3d922441b40265c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668292"
---
# <span data-ttu-id="d9bbb-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="d9bbb-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="d9bbb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bbb-103">A Web App-bővítőhely konfigurációs neveinek beállítása</span><span class="sxs-lookup"><span data-stu-id="d9bbb-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="d9bbb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9bbb-104">SYNTAX</span></span>

### <span data-ttu-id="d9bbb-105">S1</span><span class="sxs-lookup"><span data-stu-id="d9bbb-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9bbb-106">S2</span><span class="sxs-lookup"><span data-stu-id="d9bbb-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9bbb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9bbb-107">DESCRIPTION</span></span>
<span data-ttu-id="d9bbb-108">A **set-AzWebAppSlotConfigName** parancsmag az App beállításait és a csatlakozási karakterláncokat bővítőhelyként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="d9bbb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d9bbb-109">EXAMPLES</span></span>

### <span data-ttu-id="d9bbb-110">1:</span><span class="sxs-lookup"><span data-stu-id="d9bbb-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="d9bbb-111">Ez a parancs eltávolítja a webalkalmazások ContosoWebApp társított összes app-beállítást és a kapcsolati karakterláncot az erőforráscsoport alapértelmezett verziójában – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="d9bbb-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d9bbb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9bbb-112">PARAMETERS</span></span>

### <span data-ttu-id="d9bbb-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="d9bbb-113">-AppSettingNames</span></span>
<span data-ttu-id="d9bbb-114">Az alkalmazás beállításai nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="d9bbb-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="d9bbb-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="d9bbb-115">-ConnectionStringNames</span></span>
<span data-ttu-id="d9bbb-116">A kapcsolati karakterláncok nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="d9bbb-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="d9bbb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bbb-117">-DefaultProfile</span></span>
<span data-ttu-id="d9bbb-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9bbb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9bbb-119">-Name</span></span>
<span data-ttu-id="d9bbb-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="d9bbb-120">WebApp Name</span></span>

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

### <span data-ttu-id="d9bbb-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="d9bbb-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="d9bbb-122">Az összes app-név eltávolítása beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d9bbb-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="d9bbb-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="d9bbb-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="d9bbb-124">Az összes kapcsolati karakterlánc nevének eltávolítása beállítás</span><span class="sxs-lookup"><span data-stu-id="d9bbb-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="d9bbb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9bbb-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9bbb-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d9bbb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d9bbb-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d9bbb-127">-WebApp</span></span>
<span data-ttu-id="d9bbb-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="d9bbb-128">WebApp Object</span></span>

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

### <span data-ttu-id="d9bbb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bbb-129">CommonParameters</span></span>
<span data-ttu-id="d9bbb-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9bbb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bbb-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9bbb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bbb-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9bbb-132">INPUTS</span></span>

### <span data-ttu-id="d9bbb-133">System. string []</span><span class="sxs-lookup"><span data-stu-id="d9bbb-133">System.String[]</span></span>

### <span data-ttu-id="d9bbb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d9bbb-134">System.String</span></span>

### <span data-ttu-id="d9bbb-135">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d9bbb-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d9bbb-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9bbb-136">OUTPUTS</span></span>

### <span data-ttu-id="d9bbb-137">Microsoft. Azure. Management. WebSites. models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="d9bbb-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="d9bbb-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9bbb-138">NOTES</span></span>

## <span data-ttu-id="d9bbb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9bbb-139">RELATED LINKS</span></span>
