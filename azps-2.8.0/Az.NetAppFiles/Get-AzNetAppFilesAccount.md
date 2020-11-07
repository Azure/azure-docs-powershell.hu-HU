---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: dbe206a744cc0a80d166d93b09ff0ab000cb3bc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837722"
---
# <span data-ttu-id="cb539-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cb539-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="cb539-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb539-102">SYNOPSIS</span></span>
<span data-ttu-id="cb539-103">Az Azure NetApp-fájlok (ANF) fiókjának adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb539-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="cb539-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb539-104">SYNTAX</span></span>

### <span data-ttu-id="cb539-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb539-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb539-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb539-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb539-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb539-107">DESCRIPTION</span></span>
<span data-ttu-id="cb539-108">A **Get-AzNetAppFilesAccount** PARANCSMAG az ANF-fiók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb539-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="cb539-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cb539-109">EXAMPLES</span></span>

### <span data-ttu-id="cb539-110">Példa 1: ANF-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="cb539-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="cb539-111">Ez a parancs a MyAnfAccount nevű fiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb539-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="cb539-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb539-112">PARAMETERS</span></span>

### <span data-ttu-id="cb539-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb539-113">-DefaultProfile</span></span>
<span data-ttu-id="cb539-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb539-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb539-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb539-115">-Name</span></span>
<span data-ttu-id="cb539-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="cb539-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb539-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb539-117">-ResourceGroupName</span></span>
<span data-ttu-id="cb539-118">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="cb539-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb539-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb539-119">-ResourceId</span></span>
<span data-ttu-id="cb539-120">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cb539-120">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb539-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb539-121">CommonParameters</span></span>
<span data-ttu-id="cb539-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb539-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cb539-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb539-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb539-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb539-124">INPUTS</span></span>

### <span data-ttu-id="cb539-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cb539-125">System.String</span></span>

## <span data-ttu-id="cb539-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb539-126">OUTPUTS</span></span>

### <span data-ttu-id="cb539-127">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cb539-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="cb539-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb539-128">NOTES</span></span>

## <span data-ttu-id="cb539-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb539-129">RELATED LINKS</span></span>
