---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 12881d387d1e98bef8ca1fa00790b0332a338b7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929306"
---
# <span data-ttu-id="ad3cb-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ad3cb-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="ad3cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3cb-103">Tiltsa le az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="ad3cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad3cb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3cb-106">A **Disable-AzStorageStaticWebsite** parancsmag letiltja az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="ad3cb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad3cb-107">EXAMPLES</span></span>

### <span data-ttu-id="ad3cb-108">1. példa: Statikus webhely letiltása Azure Storage-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="ad3cb-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="ad3cb-109">Ez a parancs letiltja az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="ad3cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-110">PARAMETERS</span></span>

### <span data-ttu-id="ad3cb-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ad3cb-111">-Context</span></span>
<span data-ttu-id="ad3cb-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="ad3cb-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="ad3cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3cb-113">-DefaultProfile</span></span>
<span data-ttu-id="ad3cb-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad3cb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad3cb-115">-PassThru</span></span>
<span data-ttu-id="ad3cb-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ad3cb-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ad3cb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad3cb-117">-Confirm</span></span>
<span data-ttu-id="ad3cb-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad3cb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad3cb-119">-WhatIf</span></span>
<span data-ttu-id="ad3cb-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad3cb-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad3cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3cb-122">CommonParameters</span></span>
<span data-ttu-id="ad3cb-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3cb-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3cb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3cb-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-125">INPUTS</span></span>

### <span data-ttu-id="ad3cb-126">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad3cb-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ad3cb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad3cb-127">OUTPUTS</span></span>

### <span data-ttu-id="ad3cb-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="ad3cb-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="ad3cb-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad3cb-129">NOTES</span></span>

## <span data-ttu-id="ad3cb-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad3cb-130">RELATED LINKS</span></span>
