---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195070"
---
# <span data-ttu-id="20cab-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="20cab-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="20cab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20cab-102">SYNOPSIS</span></span>
<span data-ttu-id="20cab-103">Tiltsa le az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="20cab-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="20cab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20cab-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20cab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20cab-105">DESCRIPTION</span></span>
<span data-ttu-id="20cab-106">A **disable-AzStorageStaticWebsite** parancsmag letiltja a statikus webhelyet az Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="20cab-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="20cab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20cab-107">EXAMPLES</span></span>

### <span data-ttu-id="20cab-108">Példa 1: a statikus webhely letiltása Azure Storage-fiók esetén</span><span class="sxs-lookup"><span data-stu-id="20cab-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="20cab-109">Ez a parancs letiltja a statikus webhelyet Azure-tároló fiók esetén.</span><span class="sxs-lookup"><span data-stu-id="20cab-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="20cab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20cab-110">PARAMETERS</span></span>

### <span data-ttu-id="20cab-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="20cab-111">-Context</span></span>
<span data-ttu-id="20cab-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="20cab-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="20cab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20cab-113">-DefaultProfile</span></span>
<span data-ttu-id="20cab-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20cab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20cab-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20cab-115">-PassThru</span></span>
<span data-ttu-id="20cab-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="20cab-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="20cab-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20cab-117">-Confirm</span></span>
<span data-ttu-id="20cab-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20cab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20cab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20cab-119">-WhatIf</span></span>
<span data-ttu-id="20cab-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20cab-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20cab-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20cab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20cab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20cab-122">CommonParameters</span></span>
<span data-ttu-id="20cab-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20cab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20cab-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20cab-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20cab-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20cab-125">INPUTS</span></span>

### <span data-ttu-id="20cab-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="20cab-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="20cab-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20cab-127">OUTPUTS</span></span>

### <span data-ttu-id="20cab-128">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="20cab-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="20cab-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20cab-129">NOTES</span></span>

## <span data-ttu-id="20cab-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20cab-130">RELATED LINKS</span></span>