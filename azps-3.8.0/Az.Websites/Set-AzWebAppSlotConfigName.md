---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: a2c57ebe6f85209596628dffe9de88ca260bbafa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012599"
---
# <span data-ttu-id="47a76-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="47a76-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="47a76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47a76-102">SYNOPSIS</span></span>
<span data-ttu-id="47a76-103">A Web App-bővítőhely konfigurációs neveinek beállítása</span><span class="sxs-lookup"><span data-stu-id="47a76-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="47a76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47a76-104">SYNTAX</span></span>

### <span data-ttu-id="47a76-105">S1</span><span class="sxs-lookup"><span data-stu-id="47a76-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47a76-106">S2</span><span class="sxs-lookup"><span data-stu-id="47a76-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47a76-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="47a76-107">DESCRIPTION</span></span>
<span data-ttu-id="47a76-108">A **set-AzWebAppSlotConfigName** parancsmag az App beállításait és a csatlakozási karakterláncokat bővítőhelyként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="47a76-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="47a76-109">Példák</span><span class="sxs-lookup"><span data-stu-id="47a76-109">EXAMPLES</span></span>

### <span data-ttu-id="47a76-110">1:</span><span class="sxs-lookup"><span data-stu-id="47a76-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="47a76-111">Ez a parancs eltávolítja a webalkalmazások ContosoWebApp társított összes app-beállítást és a kapcsolati karakterláncot az erőforráscsoport alapértelmezett verziójában – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="47a76-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="47a76-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47a76-112">PARAMETERS</span></span>

### <span data-ttu-id="47a76-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="47a76-113">-AppSettingNames</span></span>
<span data-ttu-id="47a76-114">Az alkalmazás beállításai nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="47a76-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="47a76-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="47a76-115">-ConnectionStringNames</span></span>
<span data-ttu-id="47a76-116">A kapcsolati karakterláncok nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="47a76-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="47a76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a76-117">-DefaultProfile</span></span>
<span data-ttu-id="47a76-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47a76-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47a76-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47a76-119">-Name</span></span>
<span data-ttu-id="47a76-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="47a76-120">WebApp Name</span></span>

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

### <span data-ttu-id="47a76-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="47a76-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="47a76-122">Az összes app-név eltávolítása beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="47a76-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="47a76-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="47a76-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="47a76-124">Az összes kapcsolati karakterlánc nevének eltávolítása beállítás</span><span class="sxs-lookup"><span data-stu-id="47a76-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="47a76-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47a76-125">-ResourceGroupName</span></span>
<span data-ttu-id="47a76-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="47a76-126">Resource Group Name</span></span>

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

### <span data-ttu-id="47a76-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="47a76-127">-WebApp</span></span>
<span data-ttu-id="47a76-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="47a76-128">WebApp Object</span></span>

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

### <span data-ttu-id="47a76-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a76-129">CommonParameters</span></span>
<span data-ttu-id="47a76-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47a76-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a76-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a76-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a76-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47a76-132">INPUTS</span></span>

### <span data-ttu-id="47a76-133">System. string []</span><span class="sxs-lookup"><span data-stu-id="47a76-133">System.String[]</span></span>

### <span data-ttu-id="47a76-134">System. String</span><span class="sxs-lookup"><span data-stu-id="47a76-134">System.String</span></span>

### <span data-ttu-id="47a76-135">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="47a76-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47a76-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47a76-136">OUTPUTS</span></span>

### <span data-ttu-id="47a76-137">Microsoft. Azure. Management. WebSites. models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="47a76-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="47a76-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47a76-138">NOTES</span></span>

## <span data-ttu-id="47a76-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47a76-139">RELATED LINKS</span></span>
