---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025659"
---
# <span data-ttu-id="698ec-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="698ec-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="698ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="698ec-102">SYNOPSIS</span></span>
<span data-ttu-id="698ec-103">A Media szolgáltatáshoz társított REST-végpont eléréséhez használt kulcs újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="698ec-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="698ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="698ec-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="698ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="698ec-105">DESCRIPTION</span></span>
<span data-ttu-id="698ec-106">A **set-AzMediaServiceKey** parancsmag újragenerálja a médiaszolgáltató által társított reprezentációs State Transfer (REST) végpont eléréséhez használt kulcsot.</span><span class="sxs-lookup"><span data-stu-id="698ec-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="698ec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="698ec-107">EXAMPLES</span></span>

### <span data-ttu-id="698ec-108">1. példa: a médiaszolgáltató eléréséhez használt elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="698ec-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="698ec-109">Ez a parancs újra létrehozta a MediaService001 nevű, a ResourceGroup004 nevű erőforráscsoport csoportjába tartozó elsődleges kulcsot.</span><span class="sxs-lookup"><span data-stu-id="698ec-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="698ec-110">2. példa: a Media szolgáltatáshoz való hozzáféréshez használt másodlagos kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="698ec-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="698ec-111">Ez a parancs újra létrehozta a MediaService002 nevű, az Resourcegroup123 nevű erőforráscsoporthoz tartozó másodlagos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="698ec-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="698ec-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="698ec-112">PARAMETERS</span></span>

### <span data-ttu-id="698ec-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="698ec-113">-AccountName</span></span>
<span data-ttu-id="698ec-114">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag újra létrehozta.</span><span class="sxs-lookup"><span data-stu-id="698ec-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698ec-115">-DefaultProfile</span></span>
<span data-ttu-id="698ec-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="698ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="698ec-117">-Típus</span><span class="sxs-lookup"><span data-stu-id="698ec-117">-KeyType</span></span>
<span data-ttu-id="698ec-118">A médiaadatfolyam-szolgáltatás kulcsának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="698ec-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="698ec-119">A paraméter elfogadható értékei a következők: elsődleges vagy másodlagos.</span><span class="sxs-lookup"><span data-stu-id="698ec-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="698ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="698ec-121">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="698ec-121">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698ec-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="698ec-122">-Confirm</span></span>
<span data-ttu-id="698ec-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="698ec-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698ec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="698ec-124">-WhatIf</span></span>
<span data-ttu-id="698ec-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="698ec-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="698ec-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="698ec-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698ec-127">CommonParameters</span></span>
<span data-ttu-id="698ec-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="698ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698ec-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698ec-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698ec-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="698ec-130">INPUTS</span></span>

### <span data-ttu-id="698ec-131">System. String</span><span class="sxs-lookup"><span data-stu-id="698ec-131">System.String</span></span>

## <span data-ttu-id="698ec-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="698ec-132">OUTPUTS</span></span>

### <span data-ttu-id="698ec-133">Microsoft. Azure. commands. Media. models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="698ec-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="698ec-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="698ec-134">NOTES</span></span>

## <span data-ttu-id="698ec-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="698ec-135">RELATED LINKS</span></span>

[<span data-ttu-id="698ec-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="698ec-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


