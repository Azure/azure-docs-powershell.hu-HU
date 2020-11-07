---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 94f81e8256af9282cdd5e09c1ab2822bf99c772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680273"
---
# <span data-ttu-id="f7861-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="f7861-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="f7861-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7861-102">SYNOPSIS</span></span>
<span data-ttu-id="f7861-103">Módosítja az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="f7861-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7861-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7861-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7861-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7861-105">DESCRIPTION</span></span>
<span data-ttu-id="f7861-106">A **set-AzureRmDataLakeStoreItemAcl** parancsmag az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési LISTÁJÁT (ACL) módosítja.</span><span class="sxs-lookup"><span data-stu-id="f7861-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f7861-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f7861-107">EXAMPLES</span></span>

### <span data-ttu-id="f7861-108">Példa 1: fájlok és mappák ACL-beállítása</span><span class="sxs-lookup"><span data-stu-id="f7861-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="f7861-109">Az első parancs beolvassa az ContosoADL-fiók gyökérkönyvtárát, majd a $ACL változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f7861-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="f7861-110">A második parancs a $ACL elérési Test.txt a fájlhoz tartozó hozzáférés-vezérlési beállításokkal.</span><span class="sxs-lookup"><span data-stu-id="f7861-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="f7861-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7861-111">PARAMETERS</span></span>

### <span data-ttu-id="f7861-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="f7861-112">-Account</span></span>
<span data-ttu-id="f7861-113">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7861-113">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7861-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="f7861-114">-Acl</span></span>
<span data-ttu-id="f7861-115">Egy fájl vagy mappa hozzáférés-vezérlési listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7861-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7861-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7861-116">-PassThru</span></span>
<span data-ttu-id="f7861-117">Jelzi, hogy az eredményül kapott ACL-t vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="f7861-117">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7861-118">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="f7861-118">-Path</span></span>
<span data-ttu-id="f7861-119">A fájl vagy mappa adattó-tároló elérési útját adja meg, a legfelső szintű könyvtárral (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="f7861-119">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7861-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7861-120">-Confirm</span></span>
<span data-ttu-id="f7861-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7861-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7861-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7861-122">-WhatIf</span></span>
<span data-ttu-id="f7861-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7861-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7861-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7861-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7861-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7861-125">-DefaultProfile</span></span>
<span data-ttu-id="f7861-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7861-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7861-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7861-127">CommonParameters</span></span>
<span data-ttu-id="f7861-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7861-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7861-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7861-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7861-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7861-130">INPUTS</span></span>

### <span data-ttu-id="f7861-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="f7861-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="f7861-132">Az "ACL" paraméter elfogadja a "DataLakeStoreItemAce []" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f7861-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="f7861-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7861-133">OUTPUTS</span></span>

### <span data-ttu-id="f7861-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="f7861-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="f7861-135">Ha a PassThru meg van adva, az ACL-bejegyzések eredményül kapott listáját fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="f7861-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="f7861-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7861-136">NOTES</span></span>

## <span data-ttu-id="f7861-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7861-137">RELATED LINKS</span></span>

