---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: ab00a1fbafc446affd30d7ae06dd0d48f0f0d04d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842674"
---
# <span data-ttu-id="9bc7a-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="9bc7a-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="9bc7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bc7a-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc7a-103">A Web App-bővítőhely konfigurációs neveinek beállítása</span><span class="sxs-lookup"><span data-stu-id="9bc7a-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="9bc7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bc7a-104">SYNTAX</span></span>

### <span data-ttu-id="9bc7a-105">S1</span><span class="sxs-lookup"><span data-stu-id="9bc7a-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc7a-106">S2</span><span class="sxs-lookup"><span data-stu-id="9bc7a-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bc7a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bc7a-107">DESCRIPTION</span></span>
<span data-ttu-id="9bc7a-108">A **set-AzWebAppSlotConfigName** parancsmag az App beállításait és a csatlakozási karakterláncokat bővítőhelyként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="9bc7a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9bc7a-109">EXAMPLES</span></span>

### <span data-ttu-id="9bc7a-110">1:</span><span class="sxs-lookup"><span data-stu-id="9bc7a-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="9bc7a-111">Ez a parancs eltávolítja a webalkalmazások ContosoWebApp társított összes app-beállítást és a kapcsolati karakterláncot az erőforráscsoport alapértelmezett verziójában – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="9bc7a-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="9bc7a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bc7a-112">PARAMETERS</span></span>

### <span data-ttu-id="9bc7a-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="9bc7a-113">-AppSettingNames</span></span>
<span data-ttu-id="9bc7a-114">Az alkalmazás beállításai nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="9bc7a-114">App Settings Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc7a-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="9bc7a-115">-ConnectionStringNames</span></span>
<span data-ttu-id="9bc7a-116">A kapcsolati karakterláncok nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="9bc7a-116">Connection String Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc7a-117">-DefaultProfile</span></span>
<span data-ttu-id="9bc7a-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bc7a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9bc7a-119">-Name</span></span>
<span data-ttu-id="9bc7a-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="9bc7a-120">WebApp Name</span></span>

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

### <span data-ttu-id="9bc7a-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="9bc7a-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="9bc7a-122">Az összes app-név eltávolítása beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9bc7a-122">Remove All App Setting Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc7a-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="9bc7a-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="9bc7a-124">Az összes kapcsolati karakterlánc nevének eltávolítása beállítás</span><span class="sxs-lookup"><span data-stu-id="9bc7a-124">Remove All Connection String Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc7a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc7a-125">-ResourceGroupName</span></span>
<span data-ttu-id="9bc7a-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9bc7a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="9bc7a-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9bc7a-127">-WebApp</span></span>
<span data-ttu-id="9bc7a-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="9bc7a-128">WebApp Object</span></span>

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

### <span data-ttu-id="9bc7a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc7a-129">CommonParameters</span></span>
<span data-ttu-id="9bc7a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bc7a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc7a-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc7a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc7a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bc7a-132">INPUTS</span></span>

### <span data-ttu-id="9bc7a-133">Webhely</span><span class="sxs-lookup"><span data-stu-id="9bc7a-133">Site</span></span>
<span data-ttu-id="9bc7a-134">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9bc7a-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9bc7a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bc7a-135">OUTPUTS</span></span>

## <span data-ttu-id="9bc7a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bc7a-136">NOTES</span></span>

## <span data-ttu-id="9bc7a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bc7a-137">RELATED LINKS</span></span>

