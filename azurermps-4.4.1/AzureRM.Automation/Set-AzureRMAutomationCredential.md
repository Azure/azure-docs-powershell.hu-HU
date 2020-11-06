---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: e2a461666edf4f06e78f2bc97f47fcb63ab1c19a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493884"
---
# <span data-ttu-id="68acb-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="68acb-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="68acb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68acb-102">SYNOPSIS</span></span>
<span data-ttu-id="68acb-103">Automatizálási hitelesítő adatok módosítása</span><span class="sxs-lookup"><span data-stu-id="68acb-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68acb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68acb-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68acb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68acb-105">DESCRIPTION</span></span>
<span data-ttu-id="68acb-106">A **set-AzureRmAutomationCredential** parancsmag **PSCredential** -objektumként módosítja a hitelesítő adatokat az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="68acb-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="68acb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68acb-107">EXAMPLES</span></span>

### <span data-ttu-id="68acb-108">Példa 1: hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="68acb-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="68acb-109">Az első parancs a felhasználónevet hozzárendeli a $User változóhoz.</span><span class="sxs-lookup"><span data-stu-id="68acb-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="68acb-110">A második parancs az egyszerű szöveges jelszót egy biztonságos karakterláncba konvertálja a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="68acb-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="68acb-111">A parancs az objektumot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="68acb-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="68acb-112">A harmadik parancs a hitelesítő adatokat $User és a $Password alapján hozza létre, majd a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="68acb-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="68acb-113">A végleges parancs módosítja a ContosoCredential nevű automatizálási hitelesítő adatokat, hogy a hitelesítő adatokat használja a $Credentialban.</span><span class="sxs-lookup"><span data-stu-id="68acb-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="68acb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68acb-114">PARAMETERS</span></span>

### <span data-ttu-id="68acb-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="68acb-115">-AutomationAccountName</span></span>
<span data-ttu-id="68acb-116">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag módosítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="68acb-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68acb-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="68acb-117">-Description</span></span>
<span data-ttu-id="68acb-118">A parancsmag által módosított hitelesítő adatok leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="68acb-118">Specifies a description for the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68acb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68acb-119">-Name</span></span>
<span data-ttu-id="68acb-120">Annak a hitelesítő adatoknak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="68acb-120">Specifies the name of the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68acb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68acb-121">-ResourceGroupName</span></span>
<span data-ttu-id="68acb-122">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez ez a parancsmag módosítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="68acb-122">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68acb-123">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="68acb-123">-Value</span></span>
<span data-ttu-id="68acb-124">A hitelesítő adatokat **PSCredential** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="68acb-124">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68acb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68acb-125">-DefaultProfile</span></span>
<span data-ttu-id="68acb-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68acb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68acb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68acb-127">CommonParameters</span></span>
<span data-ttu-id="68acb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68acb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68acb-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68acb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68acb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68acb-130">INPUTS</span></span>

## <span data-ttu-id="68acb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68acb-131">OUTPUTS</span></span>

### <span data-ttu-id="68acb-132">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="68acb-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="68acb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68acb-133">NOTES</span></span>

## <span data-ttu-id="68acb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68acb-134">RELATED LINKS</span></span>

[<span data-ttu-id="68acb-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="68acb-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="68acb-136">Új – AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="68acb-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="68acb-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="68acb-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


