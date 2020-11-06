---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492440"
---
# <span data-ttu-id="731e4-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="731e4-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="731e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="731e4-102">SYNOPSIS</span></span>
<span data-ttu-id="731e4-103">A Web App-bővítőhely konfigurációs neveinek beállítása</span><span class="sxs-lookup"><span data-stu-id="731e4-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="731e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="731e4-104">SYNTAX</span></span>

### <span data-ttu-id="731e4-105">S1</span><span class="sxs-lookup"><span data-stu-id="731e4-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="731e4-106">S2</span><span class="sxs-lookup"><span data-stu-id="731e4-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="731e4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="731e4-107">DESCRIPTION</span></span>
<span data-ttu-id="731e4-108">A **set-AzureRmWebAppSlotConfigName** parancsmag az App beállításait és a csatlakozási karakterláncokat bővítőhelyként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="731e4-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="731e4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="731e4-109">EXAMPLES</span></span>

### <span data-ttu-id="731e4-110">1:</span><span class="sxs-lookup"><span data-stu-id="731e4-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="731e4-111">Ez a parancs eltávolítja a webalkalmazások ContosoWebApp társított összes app-beállítást és a kapcsolati karakterláncot az erőforráscsoport alapértelmezett verziójában – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="731e4-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="731e4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="731e4-112">PARAMETERS</span></span>

### <span data-ttu-id="731e4-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="731e4-113">-AppSettingNames</span></span>
<span data-ttu-id="731e4-114">Az alkalmazás beállításai nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="731e4-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="731e4-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="731e4-115">-ConnectionStringNames</span></span>
<span data-ttu-id="731e4-116">A kapcsolati karakterláncok nevei karakterlánc-tömb</span><span class="sxs-lookup"><span data-stu-id="731e4-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="731e4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="731e4-117">-Name</span></span>
<span data-ttu-id="731e4-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="731e4-118">WebApp Name</span></span>

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

### <span data-ttu-id="731e4-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="731e4-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="731e4-120">Az összes app-név eltávolítása beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="731e4-120">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="731e4-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="731e4-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="731e4-122">Az összes kapcsolati karakterlánc nevének eltávolítása beállítás</span><span class="sxs-lookup"><span data-stu-id="731e4-122">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="731e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="731e4-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="731e4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="731e4-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="731e4-125">-WebApp</span></span>
<span data-ttu-id="731e4-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="731e4-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731e4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731e4-127">-DefaultProfile</span></span>
<span data-ttu-id="731e4-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="731e4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="731e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731e4-129">CommonParameters</span></span>
<span data-ttu-id="731e4-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="731e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731e4-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731e4-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="731e4-132">INPUTS</span></span>

### <span data-ttu-id="731e4-133">Webhely</span><span class="sxs-lookup"><span data-stu-id="731e4-133">Site</span></span>
<span data-ttu-id="731e4-134">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="731e4-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="731e4-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="731e4-135">OUTPUTS</span></span>

## <span data-ttu-id="731e4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="731e4-136">NOTES</span></span>

## <span data-ttu-id="731e4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="731e4-137">RELATED LINKS</span></span>

