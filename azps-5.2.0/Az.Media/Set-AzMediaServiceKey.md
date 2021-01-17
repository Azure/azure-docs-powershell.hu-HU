---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339498"
---
# <span data-ttu-id="df470-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="df470-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="df470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df470-102">SYNOPSIS</span></span>
<span data-ttu-id="df470-103">A médiaszolgáltatáshoz társított REST-végpont eléréséhez használt kulcs újragenerálásával.</span><span class="sxs-lookup"><span data-stu-id="df470-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="df470-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df470-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df470-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df470-105">DESCRIPTION</span></span>
<span data-ttu-id="df470-106">A **Set-AzMediaServiceKey** parancsmag a médiaszolgáltatáshoz társított Representational State Transfer (REST) végpont eléréséhez használt kulcsot újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="df470-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="df470-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df470-107">EXAMPLES</span></span>

### <span data-ttu-id="df470-108">1. példa: A médiaszolgáltatás eléréséhez használt elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="df470-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="df470-109">Ez a parancs a MediaService001 nevű médiaszolgáltatás elsődleges kulcsát újra létrehozza, amely az ResourceGroup004 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="df470-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="df470-110">2. példa: A médiaszolgáltatás eléréséhez használt másodlagos kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="df470-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="df470-111">Ez a parancs újra létrehozza a MediaService002 nevű médiaszolgáltatás másodlagos kulcsát, amely az Resourcegroup123 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="df470-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="df470-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df470-112">PARAMETERS</span></span>

### <span data-ttu-id="df470-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df470-113">-AccountName</span></span>
<span data-ttu-id="df470-114">A parancsmag által újragenerált médiaszolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df470-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="df470-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df470-115">-DefaultProfile</span></span>
<span data-ttu-id="df470-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="df470-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df470-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="df470-117">-KeyType</span></span>
<span data-ttu-id="df470-118">Az médiaszolgáltatás kulcstípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="df470-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="df470-119">A paraméter elfogadható értékei a következőek: Elsődleges vagy Másodlagos.</span><span class="sxs-lookup"><span data-stu-id="df470-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="df470-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df470-120">-ResourceGroupName</span></span>
<span data-ttu-id="df470-121">Annak az erőforráscsoportnak a nevét adja meg, amely az médiaszolgáltatást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="df470-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="df470-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df470-122">-Confirm</span></span>
<span data-ttu-id="df470-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df470-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df470-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df470-124">-WhatIf</span></span>
<span data-ttu-id="df470-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df470-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df470-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df470-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df470-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df470-127">CommonParameters</span></span>
<span data-ttu-id="df470-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df470-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df470-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df470-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df470-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df470-130">INPUTS</span></span>

### <span data-ttu-id="df470-131">System.String</span><span class="sxs-lookup"><span data-stu-id="df470-131">System.String</span></span>

## <span data-ttu-id="df470-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df470-132">OUTPUTS</span></span>

### <span data-ttu-id="df470-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="df470-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="df470-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df470-134">NOTES</span></span>

## <span data-ttu-id="df470-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df470-135">RELATED LINKS</span></span>

[<span data-ttu-id="df470-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="df470-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


