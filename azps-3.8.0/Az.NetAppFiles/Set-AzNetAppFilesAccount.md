---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: d2a379567ab96f5776b55c4cfbac2eabeaeb02a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845029"
---
# <span data-ttu-id="064da-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="064da-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="064da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="064da-102">SYNOPSIS</span></span>
<span data-ttu-id="064da-103">Az Azure NetApp-fájlok (ANF) fiókját frissíti az új adatkészlettel.</span><span class="sxs-lookup"><span data-stu-id="064da-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="064da-104">Hasznos a kapcsolódó Active könyvtárak törléséhez.</span><span class="sxs-lookup"><span data-stu-id="064da-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="064da-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="064da-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="064da-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="064da-106">DESCRIPTION</span></span>
<span data-ttu-id="064da-107">A **set-AzNetAppFilesAccount** PARANCSMAG a ANF-fiókot módosítja.</span><span class="sxs-lookup"><span data-stu-id="064da-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="064da-108">Példák</span><span class="sxs-lookup"><span data-stu-id="064da-108">EXAMPLES</span></span>

### <span data-ttu-id="064da-109">Példa 1: ANF-fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="064da-109">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="064da-110">Ez a parancs egy frissítést hajt végre az adott fiókban.</span><span class="sxs-lookup"><span data-stu-id="064da-110">This command performs an update on the given account.</span></span> <span data-ttu-id="064da-111">Az Active Directory hiánya azt jelenti, hogy az törlődik a fiókból.</span><span class="sxs-lookup"><span data-stu-id="064da-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="064da-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="064da-112">PARAMETERS</span></span>

### <span data-ttu-id="064da-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="064da-113">-ActiveDirectories</span></span>
<span data-ttu-id="064da-114">Az aktív könyvtárakat reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="064da-114">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064da-115">-DefaultProfile</span></span>
<span data-ttu-id="064da-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="064da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="064da-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="064da-117">-Location</span></span>
<span data-ttu-id="064da-118">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="064da-118">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064da-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="064da-119">-Name</span></span>
<span data-ttu-id="064da-120">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="064da-120">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064da-121">-ResourceGroupName</span></span>
<span data-ttu-id="064da-122">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="064da-122">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064da-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="064da-123">-Tag</span></span>
<span data-ttu-id="064da-124">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="064da-124">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064da-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="064da-125">-Confirm</span></span>
<span data-ttu-id="064da-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="064da-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064da-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="064da-127">-WhatIf</span></span>
<span data-ttu-id="064da-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="064da-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="064da-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="064da-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064da-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064da-130">CommonParameters</span></span>
<span data-ttu-id="064da-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="064da-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="064da-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="064da-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064da-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="064da-133">INPUTS</span></span>

### <span data-ttu-id="064da-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="064da-134">None</span></span>

## <span data-ttu-id="064da-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="064da-135">OUTPUTS</span></span>

### <span data-ttu-id="064da-136">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="064da-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="064da-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="064da-137">NOTES</span></span>

## <span data-ttu-id="064da-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="064da-138">RELATED LINKS</span></span>
