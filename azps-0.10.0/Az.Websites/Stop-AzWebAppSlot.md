---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 4ac4482cb5972553b1dad3972200d2f0eb032fe4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842646"
---
# <span data-ttu-id="6a46c-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6a46c-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="6a46c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a46c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a46c-103">Azure Web App-bővítőhely leállítása</span><span class="sxs-lookup"><span data-stu-id="6a46c-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="6a46c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a46c-104">SYNTAX</span></span>

### <span data-ttu-id="6a46c-105">S1</span><span class="sxs-lookup"><span data-stu-id="6a46c-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a46c-106">S2</span><span class="sxs-lookup"><span data-stu-id="6a46c-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a46c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a46c-107">DESCRIPTION</span></span>
<span data-ttu-id="6a46c-108">A **stop-AzWebAppSlot** parancsmag egy Azure Web App-bővítőhelyet állít le.</span><span class="sxs-lookup"><span data-stu-id="6a46c-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="6a46c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6a46c-109">EXAMPLES</span></span>

### <span data-ttu-id="6a46c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a46c-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="6a46c-111">Ez a parancs leállítja a ContosoWebApp nevű Slot001 tartozó, a Default-Web-WestUS nevű erőforráscsoport számára tartozó bővítőhelyet.</span><span class="sxs-lookup"><span data-stu-id="6a46c-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6a46c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a46c-112">PARAMETERS</span></span>

### <span data-ttu-id="6a46c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a46c-113">-DefaultProfile</span></span>
<span data-ttu-id="6a46c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a46c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a46c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a46c-115">-Name</span></span>
<span data-ttu-id="6a46c-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="6a46c-116">WebApp Name</span></span>

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

### <span data-ttu-id="6a46c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a46c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6a46c-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="6a46c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6a46c-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6a46c-119">-Slot</span></span>
<span data-ttu-id="6a46c-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="6a46c-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6a46c-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6a46c-121">-WebApp</span></span>
<span data-ttu-id="6a46c-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="6a46c-122">WebApp Object</span></span>

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

### <span data-ttu-id="6a46c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a46c-123">CommonParameters</span></span>
<span data-ttu-id="6a46c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a46c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a46c-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a46c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a46c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a46c-126">INPUTS</span></span>

### <span data-ttu-id="6a46c-127">Webhely</span><span class="sxs-lookup"><span data-stu-id="6a46c-127">Site</span></span>
<span data-ttu-id="6a46c-128">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6a46c-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6a46c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a46c-129">OUTPUTS</span></span>

## <span data-ttu-id="6a46c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a46c-130">NOTES</span></span>

## <span data-ttu-id="6a46c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a46c-131">RELATED LINKS</span></span>

