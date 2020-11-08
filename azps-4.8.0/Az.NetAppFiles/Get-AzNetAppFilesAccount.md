---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024673"
---
# <span data-ttu-id="5a929-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5a929-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="5a929-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a929-102">SYNOPSIS</span></span>
<span data-ttu-id="5a929-103">Az Azure NetApp-fájlok (ANF) fiókjának adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5a929-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="5a929-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a929-104">SYNTAX</span></span>

### <span data-ttu-id="5a929-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a929-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a929-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a929-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a929-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a929-107">DESCRIPTION</span></span>
<span data-ttu-id="5a929-108">A **Get-AzNetAppFilesAccount** PARANCSMAG az ANF-fiók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5a929-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="5a929-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5a929-109">EXAMPLES</span></span>

### <span data-ttu-id="5a929-110">Példa 1: ANF-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="5a929-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="5a929-111">Ez a parancs a MyAnfAccount nevű fiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5a929-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="5a929-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a929-112">PARAMETERS</span></span>

### <span data-ttu-id="5a929-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a929-113">-DefaultProfile</span></span>
<span data-ttu-id="5a929-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a929-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a929-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a929-115">-Name</span></span>
<span data-ttu-id="5a929-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="5a929-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a929-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a929-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a929-118">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="5a929-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a929-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a929-119">-ResourceId</span></span>
<span data-ttu-id="5a929-120">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5a929-120">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a929-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a929-121">CommonParameters</span></span>
<span data-ttu-id="5a929-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a929-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a929-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5a929-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a929-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a929-124">INPUTS</span></span>

### <span data-ttu-id="5a929-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5a929-125">System.String</span></span>

## <span data-ttu-id="5a929-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a929-126">OUTPUTS</span></span>

### <span data-ttu-id="5a929-127">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5a929-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5a929-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a929-128">NOTES</span></span>

## <span data-ttu-id="5a929-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a929-129">RELATED LINKS</span></span>
