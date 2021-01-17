---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480421"
---
# <span data-ttu-id="affd7-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="affd7-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="affd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="affd7-102">SYNOPSIS</span></span>
<span data-ttu-id="affd7-103">Az eseményindító előfizetésének állapotának lekérte a megadott külső szolgáltatási eseményekre.</span><span class="sxs-lookup"><span data-stu-id="affd7-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="affd7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="affd7-104">SYNTAX</span></span>

### <span data-ttu-id="affd7-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="affd7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="affd7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="affd7-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="affd7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="affd7-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="affd7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="affd7-108">DESCRIPTION</span></span>
<span data-ttu-id="affd7-109">Ez a parancs az eseményindító előfizetésének állapotát kapja meg a megadott külső szolgáltatásesemények számára.</span><span class="sxs-lookup"><span data-stu-id="affd7-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="affd7-110">Az eseményindító csak akkor indítható el, ha a visszaadott állapot "Engedélyezve" állapotú.</span><span class="sxs-lookup"><span data-stu-id="affd7-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="affd7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="affd7-111">EXAMPLES</span></span>

### <span data-ttu-id="affd7-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="affd7-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="affd7-113">Ez a parancs a BlobEnetTrigger1-eseményindítóra vonatkozó előfizetés állapotát fogja kapni a külső szolgáltatásesemények számára.</span><span class="sxs-lookup"><span data-stu-id="affd7-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="affd7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="affd7-114">PARAMETERS</span></span>

### <span data-ttu-id="affd7-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="affd7-115">-DataFactoryName</span></span>
<span data-ttu-id="affd7-116">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="affd7-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affd7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affd7-117">-DefaultProfile</span></span>
<span data-ttu-id="affd7-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="affd7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affd7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="affd7-119">-InputObject</span></span>
<span data-ttu-id="affd7-120">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="affd7-120">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="affd7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="affd7-121">-Name</span></span>
<span data-ttu-id="affd7-122">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="affd7-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affd7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="affd7-123">-ResourceGroupName</span></span>
<span data-ttu-id="affd7-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="affd7-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affd7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="affd7-125">-ResourceId</span></span>
<span data-ttu-id="affd7-126">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="affd7-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affd7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affd7-127">CommonParameters</span></span>
<span data-ttu-id="affd7-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="affd7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affd7-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="affd7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affd7-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="affd7-130">INPUTS</span></span>

### <span data-ttu-id="affd7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="affd7-131">System.String</span></span>
<span data-ttu-id="affd7-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="affd7-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="affd7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="affd7-133">OUTPUTS</span></span>

### <span data-ttu-id="affd7-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="affd7-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="affd7-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="affd7-135">NOTES</span></span>

## <span data-ttu-id="affd7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="affd7-136">RELATED LINKS</span></span>

