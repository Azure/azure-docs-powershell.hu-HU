---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 2b0e8564f2a536c7b7eda5b9ae8ae3cc58bf41cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672637"
---
# <span data-ttu-id="5890c-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="5890c-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="5890c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5890c-102">SYNOPSIS</span></span>
<span data-ttu-id="5890c-103">A Media szolgáltatáshoz társított REST-végpont eléréséhez használt kulcs újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="5890c-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5890c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5890c-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5890c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5890c-105">DESCRIPTION</span></span>
<span data-ttu-id="5890c-106">A **set-AzureRmMediaServiceKey** parancsmag újragenerálja a médiaszolgáltató által társított reprezentációs State Transfer (REST) végpont eléréséhez használt kulcsot.</span><span class="sxs-lookup"><span data-stu-id="5890c-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="5890c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5890c-107">EXAMPLES</span></span>

### <span data-ttu-id="5890c-108">1. példa: a médiaszolgáltató eléréséhez használt elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="5890c-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="5890c-109">Ez a parancs újra létrehozta a MediaService001 nevű, a ResourceGroup004 nevű erőforráscsoport csoportjába tartozó elsődleges kulcsot.</span><span class="sxs-lookup"><span data-stu-id="5890c-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="5890c-110">2. példa: a Media szolgáltatáshoz való hozzáféréshez használt másodlagos kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="5890c-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="5890c-111">Ez a parancs újra létrehozta a MediaService002 nevű, az Resourcegroup123 nevű erőforráscsoporthoz tartozó másodlagos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="5890c-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="5890c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5890c-112">PARAMETERS</span></span>

### <span data-ttu-id="5890c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5890c-113">-AccountName</span></span>
<span data-ttu-id="5890c-114">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag újra létrehozta.</span><span class="sxs-lookup"><span data-stu-id="5890c-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5890c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5890c-115">-DefaultProfile</span></span>
<span data-ttu-id="5890c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5890c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5890c-117">-Típus</span><span class="sxs-lookup"><span data-stu-id="5890c-117">-KeyType</span></span>
<span data-ttu-id="5890c-118">A médiaadatfolyam-szolgáltatás kulcsának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5890c-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="5890c-119">A paraméter elfogadható értékei a következők: elsődleges vagy másodlagos.</span><span class="sxs-lookup"><span data-stu-id="5890c-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5890c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5890c-120">-ResourceGroupName</span></span>
<span data-ttu-id="5890c-121">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5890c-121">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5890c-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5890c-122">-Confirm</span></span>
<span data-ttu-id="5890c-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5890c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5890c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5890c-124">-WhatIf</span></span>
<span data-ttu-id="5890c-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5890c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5890c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5890c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5890c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5890c-127">CommonParameters</span></span>
<span data-ttu-id="5890c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5890c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5890c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5890c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5890c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5890c-130">INPUTS</span></span>

### <span data-ttu-id="5890c-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="5890c-131">None</span></span>
<span data-ttu-id="5890c-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5890c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5890c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5890c-133">OUTPUTS</span></span>

### <span data-ttu-id="5890c-134">Microsoft. Azure. commands. Media. models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="5890c-134">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="5890c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5890c-135">NOTES</span></span>

## <span data-ttu-id="5890c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5890c-136">RELATED LINKS</span></span>

[<span data-ttu-id="5890c-137">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="5890c-137">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)


