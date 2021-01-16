---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349805"
---
# <span data-ttu-id="c0c01-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c0c01-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="c0c01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c01-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c01-103">Tiltsa le az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="c0c01-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c0c01-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0c01-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c01-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0c01-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c01-106">A **Disable-AzStorageStaticWebsite** parancsmag letiltja az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="c0c01-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c0c01-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0c01-107">EXAMPLES</span></span>

### <span data-ttu-id="c0c01-108">1. példa: Statikus webhely letiltása Azure Storage-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="c0c01-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="c0c01-109">Ez a parancs letiltja az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="c0c01-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="c0c01-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0c01-110">PARAMETERS</span></span>

### <span data-ttu-id="c0c01-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c0c01-111">-Context</span></span>
<span data-ttu-id="c0c01-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="c0c01-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c0c01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c01-113">-DefaultProfile</span></span>
<span data-ttu-id="c0c01-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0c01-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c01-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0c01-115">-PassThru</span></span>
<span data-ttu-id="c0c01-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c0c01-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c0c01-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0c01-117">-Confirm</span></span>
<span data-ttu-id="c0c01-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c0c01-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c01-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c01-119">-WhatIf</span></span>
<span data-ttu-id="c0c01-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c0c01-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c01-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0c01-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c01-122">CommonParameters</span></span>
<span data-ttu-id="c0c01-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c01-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c01-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c01-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0c01-125">INPUTS</span></span>

### <span data-ttu-id="c0c01-126">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0c01-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c0c01-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0c01-127">OUTPUTS</span></span>

### <span data-ttu-id="c0c01-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="c0c01-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="c0c01-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0c01-129">NOTES</span></span>

## <span data-ttu-id="c0c01-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0c01-130">RELATED LINKS</span></span>
