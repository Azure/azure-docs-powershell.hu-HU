---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 4d5a12136dc23375e7ac5ea822c663c018f3bf68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668701"
---
# <span data-ttu-id="17d01-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="17d01-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="17d01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17d01-102">SYNOPSIS</span></span>
<span data-ttu-id="17d01-103">Tiltsa le az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="17d01-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="17d01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17d01-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17d01-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17d01-105">DESCRIPTION</span></span>
<span data-ttu-id="17d01-106">A **disable-AzStorageStaticWebsite** parancsmag letiltja a statikus webhelyet az Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="17d01-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="17d01-107">Példák</span><span class="sxs-lookup"><span data-stu-id="17d01-107">EXAMPLES</span></span>

### <span data-ttu-id="17d01-108">Példa 1: a statikus webhely letiltása Azure Storage-fiók esetén</span><span class="sxs-lookup"><span data-stu-id="17d01-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="17d01-109">Ez a parancs letiltja a statikus webhelyet Azure-tároló fiók esetén.</span><span class="sxs-lookup"><span data-stu-id="17d01-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="17d01-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17d01-110">PARAMETERS</span></span>

### <span data-ttu-id="17d01-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="17d01-111">-Context</span></span>
<span data-ttu-id="17d01-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="17d01-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17d01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d01-113">-DefaultProfile</span></span>
<span data-ttu-id="17d01-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17d01-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d01-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17d01-115">-PassThru</span></span>
<span data-ttu-id="17d01-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="17d01-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d01-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17d01-117">-Confirm</span></span>
<span data-ttu-id="17d01-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17d01-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d01-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17d01-119">-WhatIf</span></span>
<span data-ttu-id="17d01-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17d01-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17d01-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17d01-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d01-122">CommonParameters</span></span>
<span data-ttu-id="17d01-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17d01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d01-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d01-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d01-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17d01-125">INPUTS</span></span>

### <span data-ttu-id="17d01-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="17d01-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="17d01-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17d01-127">OUTPUTS</span></span>

### <span data-ttu-id="17d01-128">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="17d01-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="17d01-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17d01-129">NOTES</span></span>

## <span data-ttu-id="17d01-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17d01-130">RELATED LINKS</span></span>
