---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025907"
---
# <span data-ttu-id="8e52a-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8e52a-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="8e52a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e52a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e52a-103">Engedélyezze az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="8e52a-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="8e52a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e52a-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e52a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e52a-105">DESCRIPTION</span></span>
<span data-ttu-id="8e52a-106">Az **enable-AzStorageStaticWebsite** parancsmag engedélyezi a statikus webhelyt az Azure Storage-fiók számára.</span><span class="sxs-lookup"><span data-stu-id="8e52a-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="8e52a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e52a-107">EXAMPLES</span></span>

### <span data-ttu-id="8e52a-108">1. példa: a statikus webhely engedélyezése az Azure tárhely-fiókjához</span><span class="sxs-lookup"><span data-stu-id="8e52a-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="8e52a-109">Ez a parancs engedélyezi az Azure Storage-fiók statikus webhelyét.</span><span class="sxs-lookup"><span data-stu-id="8e52a-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="8e52a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e52a-110">PARAMETERS</span></span>

### <span data-ttu-id="8e52a-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8e52a-111">-Context</span></span>
<span data-ttu-id="8e52a-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="8e52a-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8e52a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e52a-113">-DefaultProfile</span></span>
<span data-ttu-id="8e52a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e52a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e52a-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="8e52a-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="8e52a-116">Annak az elérési útnak az elérési útvonala, amelyet meg kell adni a 404 kiadásakor (vagyis ha a böngésző olyan lapot kér, amely nem létezik.)</span><span class="sxs-lookup"><span data-stu-id="8e52a-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="8e52a-117">-IndexDocument</span></span>
<span data-ttu-id="8e52a-118">A tárgymutató-dokumentum neve az egyes könyvtárakban.</span><span class="sxs-lookup"><span data-stu-id="8e52a-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e52a-119">-PassThru</span></span>
<span data-ttu-id="8e52a-120">Statikus webhely beállítása az ServiceProperties-on</span><span class="sxs-lookup"><span data-stu-id="8e52a-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="8e52a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e52a-121">-Confirm</span></span>
<span data-ttu-id="8e52a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e52a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e52a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e52a-123">-WhatIf</span></span>
<span data-ttu-id="8e52a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e52a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e52a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e52a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e52a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e52a-126">CommonParameters</span></span>
<span data-ttu-id="8e52a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e52a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e52a-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e52a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e52a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e52a-129">INPUTS</span></span>

### <span data-ttu-id="8e52a-130">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8e52a-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8e52a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e52a-131">OUTPUTS</span></span>

### <span data-ttu-id="8e52a-132">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="8e52a-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="8e52a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e52a-133">NOTES</span></span>

## <span data-ttu-id="8e52a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e52a-134">RELATED LINKS</span></span>
